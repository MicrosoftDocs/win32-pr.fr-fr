---
title: Règles d’utilisation des pointeurs
description: le portage de votre code pour la compilation pour les Windows Microsoft 32 et 64 bits est simple. Vous devez uniquement suivre quelques règles simples concernant les pointeurs de Cast et utiliser les nouveaux types de données dans votre code. Les règles de manipulation des pointeurs sont les suivantes.
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- règles d’utilisation des pointeurs 64-bit Windows programmation
- manipulation de pointeurs 64 bits Windows programmation
- programmation de pointeurs de casting 64 bits Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416127"
---
# <a name="rules-for-using-pointers"></a>Règles d’utilisation des pointeurs

le portage de votre code pour la compilation pour les Windows Microsoft 32 et 64 bits est simple. Vous devez uniquement suivre quelques règles simples concernant les pointeurs de Cast et utiliser les nouveaux types de données dans votre code. Les règles de manipulation des pointeurs sont les suivantes.

1.  N’effectuez pas de cast des pointeurs vers **int**, **long**, **ULong** ou **DWORD**.

    Si vous devez effectuer un cast d’un pointeur pour tester certains bits, définir ou effacer des bits, ou encore manipuler son contenu, utilisez le type PTR **\_ ptr** ou **int \_ ptr** . ces types sont des types intégraux qui s’adaptent à la taille d’un pointeur pour les Windows 32 et 64 bits (par exemple, **ULONG** pour 32 bits Windows et \_ int64 pour 64 bits Windows). Par exemple, supposons que vous portiez le code suivant :

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    Dans le cadre du processus de Portage, vous devez modifier le code comme suit :

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    Utilisez **uint \_ ptr** et **int \_ ptr** le cas échéant (et si vous n’êtes pas certain qu’ils sont requis, il n’y a pas de danger de les utiliser uniquement dans le cas présent). N’effectuez pas de cast de vos pointeurs vers les types **ULong**, **long**, **int**, **uint** ou **DWORD**.

    Notez que **descripteur** est défini en tant que **void _. par \* *conséquent, Cast a _* handle** value vers une valeur **ULong** pour tester, définir ou effacer les bits de poids faible est une erreur sur le Windows bits 64.

2.  Utilisez la fonction **PtrToLong** ou **PtrToUlong** pour tronquer les pointeurs.

    Si vous devez tronquer un pointeur vers une valeur 32 bits, utilisez la fonction **PtrToLong** ou **PtrToUlong** (définie dans Basetsd. h). Ces fonctions désactivent l’avertissement de troncation de pointeur pour la durée de l’appel.

    Utilisez ces fonctions avec précaution. Une fois que vous avez converti une variable pointeur à l’aide de l’une de ces fonctions, ne l’utilisez jamais comme pointeur. Ces fonctions tronquent les 32 bits supérieurs d’une adresse, qui sont généralement nécessaires pour accéder à la mémoire référencée à l’origine par le pointeur. L’utilisation de ces fonctions sans tenir compte de la prudence entraînera un code fragile.

3.  Soyez prudent lorsque vous utilisez \_ des valeurs de pointeur 32 dans du code qui peuvent être compilées en tant que code 64 bits. Le compilateur signera l’extension du pointeur lorsqu’il sera assigné à un pointeur natif dans le code 64 bits, et non pas à l’extension du pointeur à zéro.
4.  Soyez prudent lorsque vous utilisez \_ des valeurs de pointeur 64 dans du code qui peuvent être compilées en tant que code 32 bits. Le compilateur signera l’extension du pointeur dans le code 32 bits, et non pas l’extension du pointeur à zéro.
5.  Veillez à utiliser des paramètres OUT.

    Supposons, par exemple, que vous ayez défini une fonction comme suit :

    `void func( OUT PULONG *PointerToUlong );`

    N’appelez pas cette fonction comme suit.

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    Utilisez plutôt l’appel suivant.

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Cast &UL à **Pulong \*** empêche une erreur du compilateur, mais la fonction écrit une valeur de pointeur 64 bits dans la mémoire au niveau de &UL. ce code fonctionne sur les Windowss 32 bits, mais entraîne une corruption des données sur les Windows 64 bits, et il s’agit d’une corruption difficile et difficile à trouver. La ligne inférieure : ne jouez pas de plis avec le code C. la solution est plus simple et simple.

6.  Soyez vigilant avec les interfaces polymorphes.

    Ne créez pas de fonctions qui acceptent des paramètres **DWORD** pour les données polymorphes. Si les données peuvent être un pointeur ou une valeur intégrale, utilisez le \_ type uint ptr ou **pVoid** .

    Par exemple, ne créez pas une fonction qui accepte un tableau de paramètres d’exception typés en tant que valeurs **DWORD** . Le tableau doit être un tableau de **valeurs \_ ptr DWORD** . Par conséquent, les éléments de tableau peuvent contenir des adresses ou des valeurs intégrales de 32 bits. (En règle générale, si le type d’origine est **DWORD** et qu’il doit être une largeur de pointeur, convertissez-le en valeur **\_ ptr DWORD** . C’est pourquoi il existe des types de pointeurs de précision correspondants.) Si vous avez du code qui utilise des types **DWORD**, **ULong** ou d’autres types 32 bits de manière polymorphe (c’est-à-dire que vous voulez vraiment que le membre de la structure ou du paramètre contienne une adresse), utilisez **uint \_ ptr** à la place du type actuel.

7.  Utilisez les nouvelles fonctions de la classe de fenêtre.

    Si vous avez des données privées de fenêtre ou de classe qui contiennent des pointeurs, votre code doit utiliser les nouvelles fonctions suivantes :

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    ces fonctions peuvent être utilisées sur les Windows 32 et 64 bits, mais elles sont requises sur 64 bits Windows. Préparez la transition à l’aide de ces fonctions maintenant.

    En outre, vous devez accéder aux pointeurs ou aux descripteurs dans les données privées de la classe à l’aide des nouvelles fonctions sur l’Windows 64 bits. Pour vous aider à trouver ces cas, les index suivants ne sont pas définis dans winuser. h pendant une compilation 64 bits :

    -   GWL \_ WNDPROC
    -   GWL \_ HINSTANCE
    -   GWL \_ HWDPARENT
    -   GWL \_ UserData

    Au lieu de cela, winuser. h définit les nouveaux index suivants :

    -   GWLP \_ WNDPROC
    -   GWLP \_ HINSTANCE
    -   GWLP \_ HWNDPARENT
    -   GWLP \_ UserData
    -   \_ID GWLP

    Par exemple, le code suivant n’est pas compilé :

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    Elle doit être modifiée comme suit :

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    Lors de la définition du membre **cbWndExtra** de la structure [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) , veillez à réserver suffisamment d’espace pour les pointeurs. Par exemple, si vous réservez actuellement des octets sizeof (DWORD) pour une valeur de pointeur, réservez les octets sizeof (DWORD \_ PTR).

8.  Accédez à toutes les données de la fenêtre et de la classe à l’aide du **\_ décalage du champ**.

    Il est courant d’accéder aux données de fenêtre à l’aide d’offsets codés en dur. Cette technique n’est pas portable pour la Windows 64 bits. Pour rendre votre code portable, accédez à votre fenêtre et à vos données de classe à l’aide de la macro **\_ offset de champ** . Ne partez pas du principe que le deuxième pointeur a un décalage de 4.

9.  Les types **lParam**, **wParam** et **LRESULT** changent de taille avec la plateforme.

    Lors de la compilation de code 64 bits, ces types sont étendus à 64 bits, car ils contiennent généralement des pointeurs ou des types intégraux. Ne combinez pas ces valeurs avec des valeurs **DWORD**, **ULong**, **uint**, **int**, **int** ou **long** . Examinez la façon dont vous utilisez ces types et assurez-vous de ne pas tronquer par inadvertance les valeurs.

 

 