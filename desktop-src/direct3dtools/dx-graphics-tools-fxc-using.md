---
title: Compilation hors connexion
description: L’outil Effect-compiler Tool (fxc.exe) est conçu pour la compilation hors connexion des nuanceurs HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- fxc, compilation hors connexion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729909"
---
# <a name="offline-compiling"></a>Compilation hors connexion

L’outil Effect-compiler Tool (fxc.exe) est conçu pour la compilation hors connexion des nuanceurs HLSL.

## <a name="compiling-with-the-current-compiler"></a>Compilation avec le compilateur actuel

Les modèles de nuanceur pris en charge par le compilateur actuel sont affichés dans [profils](dx-graphics-tools-fxc-syntax.md). Cet exemple compile un nuanceur de pixels pour la cible du modèle de nuanceur 5,1.

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Dans cet exemple :

-   PS \_ 5 \_ 1 est le profil cible.
-   PixelShader1. fxc est le fichier objet de sortie contenant le nuanceur compilé.
-   PixelShader1. HLSL est la source.

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

Les options de débogage incluent des options supplémentaires pour désactiver les optimisations du compilateur (OD) et activer les informations de débogage (ZI) comme les numéros de ligne et les symboles.

Pour obtenir la liste complète des options de ligne de commande, consultez la page [syntaxe](dx-graphics-tools-fxc-syntax.md) .

## <a name="compiling-with-the-legacy-compiler"></a>Compilation avec le compilateur hérité

À partir de Direct3D 10, certains modèles de nuanceur ne sont plus pris en charge. Celles-ci incluent les modèles de nuanceur de pixels : PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 et PS \_ 1 \_ 4 qui prennent en charge des ressources très limitées et qui dépendent du matériel. Le compilateur a été repensé avec le modèle de nuanceur 2 (ou supérieur), ce qui permet d’améliorer l’efficacité de la compilation. Cela implique que vous soyez en cours d’exécution sur du matériel qui prend en charge les modèles de nuanceur 2 et versions ultérieures.

Notez également que vous devez consulter les notes de publication du kit de développement logiciel (SDK) associées à votre version du compilateur FXC pour le comportement affecté par le commutateur/GEC.

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a>Utilisation de l’outil Effect-compiler dans un sous-processus

Si fxc.exe est généré en tant que sous-processus par une application, il est important de s’assurer que l’application recherche et lit les données dans les canaux de sortie ou d’erreur transmis à la fonction CreateProcess. Si l’application attend uniquement que le sous-processus se termine et que l’un des canaux soit plein, le sous-processus ne se terminera jamais.

L’exemple de code suivant illustre l’attente d’un sous-processus et la lecture des canaux de sortie et d’erreur attachés au sous-processus. Le contenu du `WaitHandles` tableau correspond aux descripteurs du sous-processus, au canal pour stdout et au canal pour stderr.

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

Pour plus d’informations sur la génération d’un processus, consultez la page de référence pour [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).

## <a name="related-topics"></a>Rubriques connexes

* [Effect-Tool du compilateur](fxc.md)