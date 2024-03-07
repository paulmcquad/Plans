# Update
My Update Plans

Create Installed Apps:

pacman -Qqe | wc -l
pacman -Qqe > packages.txt

Filter Apps:

sudo pacman -S --needed - < packages.txt

Sort Apps:

sudo pacman -S --needed $(comm -12 <(pacman -Slq | sort) < (sort packages.txt)) 