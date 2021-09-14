---
title: Indications de sécurité
description: Il est important de tenir l’utilisateur informé des problèmes de sécurité possibles.
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216729"
---
# <a name="security-guideline"></a>Indications de sécurité

Il est important de tenir l’utilisateur informé des problèmes de sécurité possibles.

## <a name="notify-the-user-of-security-related-events"></a>Notifier l’utilisateur de Security-Related événements

Informez toujours l’utilisateur de toute modification de la sécurité, qu’il s’agisse d’une erreur liée à la sécurité, telle qu’un échec de certificat ou d’une modification de la sécurité du protocole sous-jacent, telle que la modification d’un site HTTPs en un site HTTP.

## <a name="notify-the-user-of-security-related-errors"></a>Notifier l’utilisateur des erreurs de Security-Related

Lorsque votre application reçoit un message d’erreur qui peut indiquer un problème de sécurité, la fonction **InternetErrorDlg** fournit une interface standard et familière pour la notification de l’utilisateur dans la plupart des cas.

Parmi les erreurs qui se trouvent dans cette catégorie, citons les suivantes :

**ERREUR \_ Internet \_ http \_ à \_ https \_ sur le \_ ReDim**

**ERREUR \_ Internet \_ non valide \_**

**ERREUR \_ Internet \_ poster \_ \_ non \_ sécurisée**

**\_Erreurs de \_ certificat Internet s \_ \_**

**ERREUR \_ de \_ certificat CN de l’Internet s \_ \_ \_ non valide**

**ERREUR \_ Internet \_ sec \_ date du certificat \_ \_ non valide**

Un échec de notification à l’utilisateur des erreurs telles que celles-ci peut exposer l’utilisateur à divers types de violations de sécurité, y compris les attaques par usurpation d’identité ou la divulgation d’informations involontaires.

## <a name="notify-the-user-when-connection-security-changes"></a>Notifier l’utilisateur lorsque la sécurité de la connexion change

Informez toujours l’utilisateur lorsque la sécurité de la connexion change, par exemple du protocole HTTPs à HTTP. Dans le cas contraire, sauf si l’utilisateur a explicitement choisi de ne pas être informé de ces modifications, vous dissimulez les risques de divulgation involontaire des informations.

Parmi les fonctions qui signalent une telle modification dans la sécurité de connexion, citons la fonction de rappel **InternetStatusCallback** et la fonction **InternetConfirmZoneCrossing** .

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 