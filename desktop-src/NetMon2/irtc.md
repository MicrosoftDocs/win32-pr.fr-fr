---
description: L’interface IRTC fournit les méthodes utilisées pour connecter le NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interface IRTC (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: f330892da5844305d4d1f3ffa3aee0bf6e9ef50fb2a1cd951c332e2b17eb3b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132928"
---
# <a name="irtc-interface"></a>Interface IRTC

L’interface **IRTC** fournit les méthodes utilisées pour connecter le NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau. **IRTC** obtient une interface aux points d’entrée locaux uniquement, qui sont nécessaires pour effectuer une capture en temps réel. Cette interface comprend une méthode qui transmet un rappel au NPP.

## <a name="members"></a>Membres

L’interface **IRTC** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRTC** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IRTC** possède ces méthodes.



| Méthode                                                              | Description                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](irtc-configure.md)                                 | Définit le déclencheur, la correspondance de modèle et la taille de mémoire tampon de la capture.<br/>                                                                             |
| [**Connecter**](irtc-connect.md)                                     | Connecte le NPP au réseau.<br/>                                                                                                             |
| [**Déconnecter**](irtc-disconnect.md)                               | Déconnecte le NPP du réseau.<br/>                                                                                                        |
| [**GetControlState**](irtc-getcontrolstate.md)                     | Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.<br/>                      |
| [**GetConversationStatistics**](irtc-getconversationstatistics.md) | Récupère les informations de [*session*](s.md) et de [*station*](s.md) pour la capture en cours.<br/> |
| [**GetTotalStatistics**](irtc-gettotalstatistics.md)               | Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.<br/>                                              |
| [**Suspendre**](irtc-pause.md)                                         | Arrête temporairement la capture en cours.<br/>                                                                                                       |
| [**QueryStations**](irtc-querystations.md)                         | Récupère une liste de tous les ordinateurs d’un sous-réseau qui utilisent Moniteur réseau pour capturer les données réseau.<br/>                                        |
| [**QueryStatus**](irtc-querystatus.md)                             | Récupère l’état du NPP.<br/>                                                                                                             |
| [**Reprendre**](irtc-resume.md)                                       | Redémarre une capture suspendue.<br/>                                                                                                                   |
| [**Activer**](irtc-start.md)                                         | Démarre une capture.<br/>                                                                                                                            |
| [**Erreur**](irtc-stop.md)                                           | Arrête la capture en cours.<br/>                                                                                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

