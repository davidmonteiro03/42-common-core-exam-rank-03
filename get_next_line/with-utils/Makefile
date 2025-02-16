# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: dcaetano <dcaetano@student.42porto.com>    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/10/24 07:31:26 by dcaetano          #+#    #+#              #
#    Updated: 2025/02/16 11:19:32 by dcaetano         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC           = cc
CFLAGS       = -Wall -Wextra -Werror
RM           = rm -rf

OBJS_DIR     = obj/
INCLUDES_DIR = ./

SRCS         = main.c get_next_line.c get_next_line_utils.c
OBJS         = $(addprefix $(OBJS_DIR), $(SRCS:.c=.o))

EXEC         = get_next_line

all: $(EXEC)

$(OBJS_DIR)%.o: ./%.c
	@mkdir -p $(dir $@)
	@$(CC) $(CFLAGS) -I$(INCLUDES_DIR) -c $< -o $@

$(OBJS_DIR)%.o: srcs/%.c
	@mkdir -p $(dir $@)
	@$(CC) $(CFLAGS) -I$(INCLUDES_DIR) -c $< -o $@

$(EXEC): $(OBJS)
	@$(CC) $(CFLAGS) -I$(INCLUDES_DIR) $^ -o $@

clean:
	@$(RM) $(OBJS_DIR)

fclean: clean
	@$(RM) $(EXEC)

re: fclean all

.PHONY: all clean fclean re
