---
description: Chargement d’un graphique à partir d’un processus externe
ms.assetid: 1c657c7f-46d7-4feb-88a7-4a3227c9070b
title: Chargement d’un graphique à partir d’un processus externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac42db3a87b00b1cb8f3a9ae5297215ae9bd3fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104550063"
---
# <a name="loading-a-graph-from-an-external-process"></a>Chargement d’un graphique à partir d’un processus externe

GraphEdit peut charger un graphique de filtre créé par un processus externe. Avec cette fonctionnalité, vous pouvez voir exactement quel graphique de filtre votre application génère, avec seulement une quantité minimale de code supplémentaire dans votre application.

> [!Note]  
> Cette fonctionnalité nécessite Windows 2000, Windows XP ou version ultérieure.

 

> [!Note]  
> À compter de Windows Vista, vous devez inscrire proppage.dll pour activer cette fonctionnalité. Proppage.dll est inclus dans le SDK Windows.

 

L’application doit inscrire l’instance du graphique de filtre dans la table ROT (Running Object Table). Le ROT est une table de recherche accessible globalement qui effectue le suivi des objets en cours d’exécution. Les objets sont enregistrés dans le ROT par moniker. Pour vous connecter au graphique, GraphEdit recherche dans le ROT les monikers dont le nom d’affichage correspond à un format particulier :


```C++
!FilterGraph X pid Y
```



où *X* est l’adresse hexadécimale du gestionnaire de graphique de filtre, et *Y* est l’ID de processus, également au format hexadécimal.

Lorsque votre application crée d’abord le graphique de filtre, appelez la fonction suivante :


```C++
HRESULT AddToRot(IUnknown *pUnkGraph, DWORD *pdwRegister) 
{
    IMoniker * pMoniker = NULL;
    IRunningObjectTable *pROT = NULL;

    if (FAILED(GetRunningObjectTable(0, &pROT))) 
    {
        return E_FAIL;
    }
    
    const size_t STRING_LENGTH = 256;

    WCHAR wsz[STRING_LENGTH];
 
   StringCchPrintfW(
        wsz, STRING_LENGTH, 
        L"FilterGraph %08x pid %08x", 
        (DWORD_PTR)pUnkGraph, 
        GetCurrentProcessId()
        );
    
    HRESULT hr = CreateItemMoniker(L"!", wsz, &pMoniker);
    if (SUCCEEDED(hr)) 
    {
        hr = pROT->Register(ROTFLAGS_REGISTRATIONKEEPSALIVE, pUnkGraph,
            pMoniker, pdwRegister);
        pMoniker->Release();
    }
    pROT->Release();
    
    return hr;
}
```



Cette fonction crée un moniker et une nouvelle entrée ROT pour le graphique de filtre. Le premier paramètre est un pointeur vers le graphique de filtre. Le deuxième paramètre reçoit une valeur qui identifie la nouvelle entrée ROT. Avant que l’application ne libère le graphique de filtre, appelez la fonction suivante pour supprimer l’entrée ROT. Le paramètre *pdwRegister* est l’identificateur retourné par la fonction AddToRot.


```C++
void RemoveFromRot(DWORD pdwRegister)
{
    IRunningObjectTable *pROT;
    if (SUCCEEDED(GetRunningObjectTable(0, &pROT))) {
        pROT->Revoke(pdwRegister);
        pROT->Release();
    }
}
```



L’exemple de code suivant montre comment appeler ces fonctions. Dans cet exemple, le code qui ajoute et supprime les entrées ROT est compilé de manière conditionnelle, afin qu’il ne soit inclus que dans les versions Debug.


```C++
IGraphBuilder *pGraph;
DWORD dwRegister;
    
// Create the filter graph manager.
CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
                        IID_IGraphBuilder, (void **)&pGraph);
#ifdef _DEBUG
hr = AddToRot(pGraph, &dwRegister);
#endif

// Rest of the application (not shown).

#ifdef _DEBUG
RemoveFromRot(dwRegister);
#endif
pGraph->Release();
```



Pour afficher le graphique de filtre dans GraphEdit, exécutez votre application et GraphEdit en même temps. Dans le menu **fichier** GraphEdit, cliquez sur **se connecter au graphique distant...** Dans la boîte de dialogue **se connecter au graphique** , sélectionnez l’ID de processus (PID) de votre application, puis cliquez sur **OK**. GraphEdit charge le graphique de filtre et l’affiche. N’utilisez pas d’autres fonctionnalités GraphEdit sur ce graphique ; cela peut entraîner des résultats inattendus. Par exemple, n’ajoutez pas ou ne supprimez pas de filtres, ou arrêtez et démarrez le graphique. Fermez GraphEdit avant de quitter votre application.

> [!Note]  
> Votre application peut atteindre plusieurs assertions lorsqu’elle se termine. Vous pouvez les ignorer.

 

L’illustration suivante montre la boîte de dialogue **se connecter au graphique** .

![se connecter au graphique](images/gedit-spy.png)

Quand GraphEdit charge le graphique, il s’exécute dans le contexte de l’application cible. Par conséquent, GraphEdit peut être bloqué, car il attend le thread. Par exemple, cela peut se produire si vous exécutez pas à pas votre code dans le débogueur.

Cette fonctionnalité doit être utilisée uniquement dans les versions Debug de votre application, et non dans les versions commerciales, car elle permet à d’autres applications d’afficher ou de contrôler le graphique de filtre.

## <a name="connecting-to-a-remote-graph-from-the-command-line"></a>Connexion à un graphique distant à partir de la ligne de commande

GraphEdit prend en charge une option de ligne de commande pour charger automatiquement un graphique distant au démarrage. La syntaxe est :


```C++
GraphEdt -a moniker
```



où *moniker* est un moniker créé à l’aide de la fonction AddToRot, décrite précédemment.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Simulation de la génération de graphiques avec GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



