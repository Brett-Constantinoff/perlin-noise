all: main

debug: main.o shader.o camera.o imgui.o 
	g++ main.o shader.o camera.o imgui_demo.o imgui_draw.o imgui_impl_glfw.o imgui_impl_opengl3.o imgui_tables.o imgui_widgets.o imgui.o -std=c++11 -g -o main -lglfw -lglew -framework OpenGL

main: main.o shader.o camera.o imgui.o 
	g++ main.o shader.o camera.o imgui_demo.o imgui_draw.o imgui_impl_glfw.o imgui_impl_opengl3.o imgui_tables.o imgui_widgets.o imgui.o -std=c++11 -o main -lglfw -lglew -framework OpenGL

main.o: main.cpp
	g++ main.cpp -std=c++11 -c

shader.o: ../shaders/shader.cpp ../shaders/shader.h
	g++ ../shaders/shader.cpp -std=c++11 -c

camera.o: ../camera/camera.cpp ../camera/camera.h
	g++ ../camera/camera.cpp -std=c++11 -c

imgui.o: ../imgui/imgui.cpp ../imgui/imgui_demo.cpp ../imgui/imgui_draw.cpp ../imgui/imgui_tables.cpp ../imgui/imgui_widgets.cpp ../imgui//imgui_impl_glfw.cpp ../imgui//imgui_impl_opengl3.cpp
	g++ ../imgui/imgui.cpp ../imgui/imgui_demo.cpp ../imgui/imgui_draw.cpp ../imgui/imgui_tables.cpp ../imgui/imgui_widgets.cpp ../imgui//imgui_impl_glfw.cpp ../imgui//imgui_impl_opengl3.cpp -std=c++11 -c

clean: 
	rm -f *.o 