   84  west build -p -d build/left -b nice_nano_v2 -- -DSHIELD=dactyl_manuform_left -DZMK_CONFIG=/workspaces/zmk-config/
   85  west build -p -d build/right -b nice_nano_v2 -- -DSHIELD=dactyl_manuform_right -DZMK_CONFIG=/workspaces/zmk-config/

   work from the zmk directory

   docker volume create --driver local -o o=bind -o type=none -o device="/home/richard/personal/zmk-config-dactyl-manuform" zmk-config

docker volume create --driver local -o o=bind -o type=none -o device="/home/richard/personal/zmk-keyboard-dactyl-manuform" zmk-modules

west build -b nice_nano_v2 -- -DSHIELD=dactyl_manuform -DZMK_EXTRA_MODULES="/workspaces/zmk-modules"