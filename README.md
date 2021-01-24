# g4d
3d in love2d

based on groverbuger's g3d 
https://github.com/groverburger/g3d

``` lua
local g4d = require('g4d')

function love.load()
  	my_model = g4d.Model('obj_file.obj', 'texture.png')
end

function love.update(dt)
	if love.keyboard.isDown('q')      then g4d.Camera:update(dt, 'left')   end
	if love.keyboard.isDown('d')      then g4d.Camera:update(dt, 'right')  end
	if love.keyboard.isDown('lshift') then g4d.Camera:update(dt, 'up')     end
	if love.keyboard.isDown('lctrl')  then g4d.Camera:update(dt, 'down')   end
	if love.keyboard.isDown('z')      then g4d.Camera:update(dt, 'toward') end
	if love.keyboard.isDown('s')      then g4d.Camera:update(dt, 'back')   end
end

function love.draw()
  	g4d:attach()
  	my_model:draw()
  	g4d:detach()
  
  	g4d:draw(0, 0)
end
```
