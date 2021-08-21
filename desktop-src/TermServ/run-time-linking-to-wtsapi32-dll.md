---
title: Run-Time la liaison à Wtsapi32.dll
description: Votre application peut utiliser l’API Services Bureau à distance pour établir une liaison dynamique avec l' Wtsapi32.dll au moment de l’exécution. Pour ce faire, votre application doit appeler la fonction LoadLibrary pour charger Wtsapi32.dll.
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc686f26029ee9bfa4332215e27a587a7e57b78de9bd0d1043ee58541ef76194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127494"
---
# <a name="run-time-linking-to-wtsapi32dll"></a>Run-Time la liaison à Wtsapi32.dll

Si votre application s’exécute dans un environnement qui n’est pas un environnement Services Bureau à distance, mais que vous souhaitez que votre application fournisse des fonctionnalités supplémentaires lorsqu’elle s’exécute dans un environnement Services Bureau à distance, l’application peut utiliser l’API Services Bureau à distance pour implémenter les fonctionnalités supplémentaires et établir une liaison dynamique avec les Wtsapi32.dll au moment de l’exécution. Pour ce faire, votre application doit appeler la fonction [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pour charger Wtsapi32.dll. Si l’appel de **LoadLibrary** échoue, votre application peut s’exécuter à l’aide de ses fonctionnalités de base. Si **LoadLibrary** s’exécute correctement, votre application peut appeler la fonction [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour récupérer les pointeurs vers les fonctions services Bureau à distance que vous souhaitez appeler.

Si votre application est conçue uniquement pour un environnement Services Bureau à distance, la liaison dynamique n’est pas nécessaire. Dans ce cas, vous pouvez inclure Wtsapi32. h et établir un lien avec Wtsapi32. lib. Ensuite, si votre application démarre dans un environnement autre que Services Bureau à distance, elle se termine car Wtsapi32.dll n’est pas présent.

Pour plus d’informations sur la façon de déterminer si votre application s’exécute dans un environnement Services Bureau à distance, consultez [détection de l’environnement services Bureau à distance](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Instructions de programmation générales](general-programming-guidelines.md)
</dt> </dl>

 

 