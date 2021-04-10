---
title: WinMain le point d’entrée de l’application
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104198902"
---
# <a name="winmain-the-application-entry-point"></a>WinMain : point d’entrée de l’application

Chaque programme Windows comprend une fonction de point d’entrée nommée **WinMain** ou **wWinMain**. Voici la signature pour **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Les quatre paramètres sont :

-   *HINSTANCE* est un événement appelé « handle vers une instance » ou « handle vers un module ». Le système d’exploitation utilise cette valeur pour identifier l’exécutable (EXE) lorsqu’il est chargé en mémoire. Le descripteur d’instance est nécessaire pour certaines fonctions Windows, par exemple pour charger des icônes ou des bitmaps.
-   *hPrevInstance* n’a aucune signification. Elle a été utilisée dans Windows 16 bits, mais elle est désormais toujours égale à zéro.
-   *pCmdLine* contient les arguments de ligne de commande sous la forme d’une chaîne Unicode.
-   *nCmdShow* est un indicateur qui indique si la fenêtre principale de l’application sera réduite, agrandie ou affichée normalement.

La fonction retourne une valeur **int** . La valeur de retour n’est pas utilisée par le système d’exploitation, mais vous pouvez utiliser la valeur de retour pour transmettre un code d’État à un autre programme que vous écrivez.

**WinAPI** est la Convention d’appel. Une *Convention d’appel* définit la manière dont une fonction reçoit des paramètres de l’appelant. Par exemple, il définit l’ordre dans lequel les paramètres apparaissent sur la pile. Veillez simplement à déclarer votre fonction **wWinMain** comme indiqué.

La fonction **WinMain** est identique à **wWinMain**, sauf que les arguments de ligne de commande sont passés comme une chaîne ANSI. La version Unicode est préférée. Vous pouvez utiliser la fonction ANSI **WinMain** même si vous compilez votre programme au format Unicode. Pour obtenir une copie Unicode des arguments de ligne de commande, appelez la fonction [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) . Cette fonction retourne tous les arguments dans une chaîne unique. Si vous souhaitez que les arguments soient un tableau de style *argv*, transmettez cette chaîne à [**CommandLineToArgvW**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

Comment le compilateur sait-il appeler **wWinMain** au lieu de la fonction **principale** standard ? Ce qui se passe réellement, c’est que la bibliothèque Microsoft C Runtime (CRT) fournit une implémentation de **main** qui appelle **WinMain** ou **wWinMain**.

> [!Note]  
> La bibliothèque CRT effectue des tâches supplémentaires dans **main**. Par exemple, tous les initialiseurs statiques sont appelés avant le **wWinMain**. Bien que vous puissiez demander à l’éditeur de liens d’utiliser une fonction de point d’entrée différente, utilisez la valeur par défaut si vous liez à la bibliothèque CRT. Sinon, le code d’initialisation du CRT sera ignoré, avec des résultats imprévisibles. (Par exemple, les objets globaux ne seront pas initialisés correctement.)

 

Voici une fonction **WinMain** vide.


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Maintenant que vous disposez du point d’entrée et que vous comprenez certaines des conventions de base et de la terminologie de base, vous êtes prêt à créer un programme de fenêtre complet.

## <a name="next"></a>Suivant

[Module 1. Votre premier programme Windows](your-first-windows-program.md).

 

 