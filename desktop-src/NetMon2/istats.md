---
description: L’interface IStats fournit les méthodes que vous utilisez pour connecter un NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau. Cette interface génère des statistiques sans frames.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interface IStats (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011530"
---
# <a name="istats-interface"></a>Interface IStats

L’interface **IStats** fournit les méthodes que vous utilisez pour connecter un NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau. Cette interface génère des statistiques sans frames.

## <a name="members"></a>Membres

L’interface **IStats** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IStats** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IStats** possède ces méthodes.



| Méthode                                                                | Description                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](istats-configure.md)                                 | Configure le déclencheur, la correspondance de modèle et la taille de mémoire tampon du fichier de capture.<br/>                                                                    |
| [**Connexion**](istats-connect.md)                                     | Connecte le NPP au réseau.<br/>                                                                                                               |
| [**Déconnecter**](istats-disconnect.md)                               | Déconnecte le NPP du réseau.<br/>                                                                                                          |
| [**GetControlState**](istats-getcontrolstate.md)                     | Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.<br/>                        |
| [**GetConversationStatistics**](istats-getconversationstatistics.md) | Récupère les informations de [*session*](s.md) et de [*station*](s.md) relatives à la capture en cours.<br/> |
| [**GetTotalStatistics**](istats-gettotalstatistics.md)               | Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.<br/>                                                |
| [**Suspendre**](istats-pause.md)                                         | Arrête temporairement la capture en cours.<br/>                                                                                                         |
| [**QueryStations**](istats-querystations.md)                         | Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.<br/>                                                  |
| [**QueryStatus**](istats-querystatus.md)                             | Récupère l’état du NPP.<br/>                                                                                                               |
| [**Sort**](istats-resume.md)                                       | Redémarre une capture suspendue.<br/>                                                                                                                     |
| [**Démarrer**](istats-start.md)                                         | Démarre la capture.<br/>                                                                                                                            |
| [**Arrêter**](istats-stop.md)                                           | Arrête la capture en cours.<br/>                                                                                                                     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

