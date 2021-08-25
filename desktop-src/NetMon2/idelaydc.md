---
description: L’interface IDelaydC fournit les méthodes utilisées pour se connecter au réseau, capturer le trafic réseau vers un fichier de capture, récupérer des statistiques et se déconnecter du réseau.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interface IDelaydC (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1b6b965990435dd7b9a1758cc9bf8ac8001c747ae800225a90123da862032ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890559"
---
# <a name="idelaydc-interface"></a>Interface IDelaydC

L’interface **IDelaydC** fournit les méthodes utilisées pour se connecter au réseau, capturer le trafic réseau vers un fichier de capture, récupérer des statistiques et se déconnecter du réseau.

Cette interface capture des frames à partir du flux de données réseau, puis copie les frames dans un fichier de capture. Cette interface est utilisée par les applications Moniteur réseau et NPP. Pour recevoir les données réseau, la carte d’interface réseau ciblée doit prendre en charge le mode de proximité.

## <a name="members"></a>Membres

L’interface **IDelaydC** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDelaydC** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDelaydC** possède ces méthodes.



| Méthode                                                                  | Description                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](idelaydc-configure.md)                                 | Envoie les informations de configuration utilisées pour une capture.<br/>                                                                                        |
| [**Connecter**](idelaydc-connect.md)                                     | Connecte le NPP au réseau.<br/>                                                                                                             |
| [**Déconnecter**](idelaydc-disconnect.md)                               | Déconnecte le NPP du réseau.<br/>                                                                                                        |
| [**GetControlState**](idelaydc-getcontrolstate.md)                     | Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.<br/>                      |
| [**GetConversationStatistics**](idelaydc-getconversationstatistics.md) | Récupère les informations de [*session*](s.md) et de [*station*](s.md) pour la capture en cours.<br/> |
| [**GetTotalStatistics**](idelaydc-gettotalstatistics.md)               | Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.<br/>                                              |
| [**Suspendre**](idelaydc-pause.md)                                         | Arrête temporairement la capture en cours.<br/>                                                                                                       |
| [**QueryStations**](idelaydc-querystations.md)                         | Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.<br/>                                                      |
| [**QueryStatus**](idelaydc-querystatus.md)                             | Récupère l’état du NPP.<br/>                                                                                                             |
| [**Reprendre**](idelaydc-resume.md)                                       | Reprend une capture suspendue.<br/>                                                                                                                    |
| [**Activer**](idelaydc-start.md)                                         | Démarre une capture et crée le [*fichier de capture*](c.md).<br/>                                                           |
| [**Erreur**](idelaydc-stop.md)                                           | Arrête la capture en cours et ferme le [*fichier de capture*](c.md).<br/>                                                   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

