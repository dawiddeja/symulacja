# symulacja

tablica = numpy.matrix(100,100)
 
 
def main():
    init_tablica()
    register_window()
 
 
def register_window():
    window = Tk()
    canvas = Canvas(window)
 
    canvas.on_click = my_on_click
 
    button_start = Button(window)
    button_start.on_click = start
 
 
def my_on_click(e):
    x = e.x
    y = e.y
 
    tablica[x,y] = tablica[x,y] * (-1)
    refresh()
 
 
def refresh():
    for punkt in tablica:
        if punkt == 1:
            color = "red"
        elif punkt == -1:
            color = blue
 
        canvas.draw_rectangle(x,y, 10, 10, fill=color)
 
 
def start():
    for punkt in tablica:
        #tutaj liczymy wartosc dla kazdego punktu
 
 
if __name__ == '__main__':
    main()
