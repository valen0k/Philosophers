NAME		=	philo_one

HEADER		=	./includes/philo_one.h

CC			=	gcc

FLAGS		=	-g -Werror -Wall -Wextra -pthread

SRCS		=	./sources/philo_one.c \
				./sources/died.c \
				./sources/parse.c \
				./sources/utils.c \
				./sources/errors.c \
				./sources/inits.c

OBJS		=	$(SRCS:%.c=%.o)

all: $(NAME)

$(NAME): $(OBJS) $(HEADER)
	@$(CC) $(FLAGS) $(OBJS) -o $(NAME)

%.o: %.c
	gcc $(FLAGS) -c $< -o $@

re	:fclean all

norm:
	norminette $(SRCS) $(HEADER)

clean:
	@rm -rf $(OBJS)

fclean: clean
	@rm $(NAME)

de:
	gcc -g -pthread $(SRCS)

.PHONY: all clean fclean re
