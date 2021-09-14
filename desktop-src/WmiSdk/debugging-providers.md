---
description: Les fournisseurs, sauf s’ils sont des fournisseurs découplés qui s’exécutent dans une application, sont chargés dans un Wmiprvse.exe processus, et non par le biais d' Svchost.exe avec un processus de Winmgmt.exe. Pour plus d’informations, consultez Hébergement et sécurité du fournisseur.
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: Fournisseurs de débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127237107"
---
# <a name="debugging-providers"></a>Fournisseurs de débogage

Les fournisseurs, sauf s’ils sont des [*fournisseurs découplés*](gloss-d.md) qui s’exécutent dans une application, sont chargés dans un Wmiprvse.exe processus, et non par le biais d' Svchost.exe avec un processus de Winmgmt.exe. Pour plus d’informations, consultez [hébergement et sécurité du fournisseur](provider-hosting-and-security.md).

lors de l’arrêt à un point d’arrêt, le débogueur Visual Studio gèle l’intégralité du processus hôte du fournisseur, qui est généralement le Wmiprvse.exe hôte partagé. Cela empêche le fonctionnement de tous les autres composants hébergés dans ce processus, y compris l’extension de Explorateur de serveurs WMI. Les applications clientes qui appellent le fournisseur sont également bloquées. les problèmes qui se produisent sont plus mauvais dans Windows 2000 et les versions antérieures, car le fournisseur est chargé dans le processus de service WMI (Winmgmt.exe).

si vous exécutez WMI Explorateur de serveurs dans une autre instance, Visual Studio IDE ne se fige pas et vous êtes en mesure de libérer le point d’arrêt. Il est recommandé d’exécuter votre fournisseur dans un processus d’hébergement distinct au cours de la phase de développement, afin que l’arrêt à un point d’arrêt bloque uniquement le processus qui héberge votre fournisseur. Les autres fonctions de WMI restent accessibles aux Explorateur de serveurs WMI et à d’autres applications ou scripts basés sur WMI. En outre, si votre fournisseur tombe en panne, il n’affecte pas le fonctionnement des autres fournisseurs chargés dans le même processus hôte.

Pour que votre fournisseur se charge dans son propre processus hôte, modifiez l’inscription du fournisseur pour définir la propriété [**\_ \_ Win32Provider. HostingModel**](--win32provider.md) sur, `NetworkServiceHost:[MyProvider]` où MyProvider peut être toute chaîne qui identifie de façon unique votre fournisseur. Par exemple, utilisez la valeur **\_ \_ Win32Provider. CLSID** . Lorsque votre fournisseur est prêt à être expédié, retournez **\_ \_ Win32Provider. HostingModel** à la valeur prévue, par exemple **NetworkServiceHost**.

Si vous n’êtes pas en train de déboguer le chargement du fournisseur, vous pouvez appeler la [**méthode Load de la \_ classe des fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) pour forcer le chargement de votre fournisseur, puis l’attacher au processus de Wmiprvse.exe qui a chargé la dll et déboguer en fonction des besoins.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
