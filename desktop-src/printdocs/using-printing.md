---
description: Cette section décrit comment imprimer à partir d’un programme de bureau Windows natif.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Impression d’applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520725"
---
# <a name="desktop-app-printing"></a>Impression d’applications de bureau

Cette section décrit comment imprimer à partir d’un programme de bureau Windows natif.

## <a name="overview"></a>Vue d’ensemble

Pour offrir une expérience utilisateur optimale lorsque vous imprimez à partir d’un programme Windows natif, le programme doit être conçu pour imprimer à partir d’un thread dédié. Dans un programme Windows natif, le programme est responsable de la gestion des événements et des messages de l’interface utilisateur. Les opérations d’impression peuvent nécessiter des périodes de calcul intense lorsque le contenu de l’application est rendu pour l’imprimante, ce qui peut empêcher le programme de répondre à l’interaction de l’utilisateur si ce traitement est effectué dans le même thread que le traitement des événements de l’interaction de l’utilisateur.

Si vous êtes déjà familiarisé avec l’écriture d’un programme Windows natif multithread, passez directement à [la rubrique Comment imprimer à partir d’une application Windows](how-to--print-from-a-windows-application.md) et comment ajouter des fonctionnalités d’impression à votre programme.

### <a name="basic-windows-program-requirements"></a>Configuration de base des programmes Windows

Pour optimiser les performances et la réactivité du programme, n’effectuez pas le traitement du travail d’impression d’un programme dans le thread qui traite l’interaction de l’utilisateur.

Cette séparation de l’interaction de l’utilisateur influencera la manière dont le programme gère les données d’application. Vous devez parfaitement comprendre ces implications avant de commencer à écrire l’application. Les rubriques suivantes décrivent les exigences de base de la gestion de l’impression dans un thread distinct d’un programme.

### <a name="windows-program-basics"></a>Notions de base des programmes Windows

Un programme Windows natif doit fournir la procédure de fenêtre principale pour traiter les messages de fenêtre qu’il reçoit du système d’exploitation. Chaque fenêtre d’un programme Windows dispose d’une fonction **WndProc** correspondante qui traite ces messages de fenêtre. Le thread dans lequel cette fonction s’exécute est appelé le thread de l’interface utilisateur ou de l’interface utilisateur.

**Utilisez des ressources pour les chaînes.**  
Utilisez des ressources de type chaîne à partir du fichier de ressources du programme plutôt que des constantes de chaîne pour les chaînes qui devront peut-être être modifiées lorsque vous prenez en charge un autre langage. Pour qu’un programme puisse utiliser une ressource de type chaîne comme chaîne, le programme doit récupérer la ressource à partir du fichier de ressources et la copier dans une mémoire tampon locale. Cela nécessite une programmation supplémentaire au début, mais permet une modification, une traduction et une localisation plus faciles du programme à l’avenir.  
**Traiter les données en étapes.**  
Traitez le travail d’impression dans les étapes qui peuvent être interrompues. Cette conception permet à l’utilisateur d’annuler une longue opération de traitement avant qu’elle ne se termine et empêche le programme de bloquer d’autres programmes qui peuvent s’exécuter en même temps.  
**Utilisez les données utilisateur de la fenêtre.**  
L’impression d’applications a souvent plusieurs fenêtres et threads. Pour conserver les données disponibles entre les threads et les étapes de traitement sans utiliser des variables globales statiques, référencez les structures de données à l’aide d’un pointeur de données qui fait partie de la fenêtre dans laquelle elles sont utilisées.  


L’exemple de code suivant montre un point d’entrée principal pour une application d’impression. Cet exemple montre comment utiliser des ressources de type chaîne à la place de constantes de chaîne et affiche également la boucle de message principale qui traite les messages de fenêtre du programme.


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a>Informations sur le document

Les programmes Windows natifs qui impriment doivent être conçus pour le traitement multithread. L’une des exigences d’une conception multithread consiste à protéger les éléments de données du programme afin qu’ils puissent être utilisés simultanément par plusieurs threads. Vous pouvez protéger les éléments de données en utilisant des objets de synchronisation et en organisant les données pour éviter les conflits entre les threads. En même temps, le programme doit empêcher toute modification des données du programme pendant son impression. L’exemple de programme utilise plusieurs techniques de programmation multithread différentes.

 **Événements de synchronisation**  
L’exemple de programme utilise des événements, des handles de thread et des fonctions Wait pour synchroniser le traitement entre le thread d’impression et le programme principal et pour indiquer que les données sont en cours d’utilisation.  
**Messages Windows spécifiques à l’application**  
L’exemple de programme utilise des messages de fenêtre spécifiques à l’application pour rendre le programme plus compatible avec d’autres programmes Windows natifs. Le fractionnement du traitement en étapes plus petites et la mise en file d’attente de ces étapes dans la boucle de message de fenêtre permet à Windows de gérer plus facilement le traitement sans bloquer d’autres applications qui peuvent également s’exécuter sur l’ordinateur.  
**Structures de données**  
L’exemple de programme n’est pas écrit dans un style orienté objet à l’aide d’objets et de classes, bien qu’il regroupe des éléments de données dans des structures de données. L’exemple n’utilise pas une approche orientée objet pour éviter d’impliquer qu’une approche est mieux ou pire qu’une autre.  
Vous pouvez utiliser les fonctions et les structures de données de l’exemple de programme comme point de départ lors de la conception de votre programme. Que vous décidiez de concevoir un programme orienté objet ou non, il est important de se rappeler que vous devez regrouper les éléments de données associés afin de pouvoir les utiliser en toute sécurité dans différents threads si nécessaire.  


### <a name="printer-device-context"></a>Contexte de périphérique d’impression

Lors de l’impression, vous souhaiterez peut-être afficher le contenu à imprimer dans un contexte de périphérique. [Comment : récupérer un contexte de périphérique d’impression](retrieving-a-printer-device-context.md) décrit les différentes façons dont vous pouvez obtenir un contexte de périphérique d’impression.

## <a name="related-topics"></a>Rubriques connexes



[Comment imprimer à partir d’une application Windows](how-to--print-from-a-windows-application.md)


 

 



