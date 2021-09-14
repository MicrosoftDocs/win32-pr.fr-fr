---
description: L’interface IESP fournit les méthodes qui connectent le NPP au réseau, capture le trafic réseau dans un fichier de capture, récupère les statistiques et déconnecte le NPP du réseau.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interface IESP (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416716"
---
# <a name="iesp-interface"></a>Interface IESP

L’interface **IESP** fournit les méthodes qui connectent le NPP au réseau, capture le trafic réseau dans un fichier de capture, récupère les statistiques et déconnecte le NPP du réseau. Cette interface est principalement utilisée lorsque vous devez collecter des [*statistiques de conversation*](c.md) réseau dans un format de fichier ESP propriétaire.

## <a name="members"></a>Membres

L’interface **IESP** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IESP** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IESP** possède ces méthodes.



| Méthode                                          | Description                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](iesp-configure.md)             | Envoie les informations de configuration d’une capture<br/>                                                                         |
| [**Connexion**](iesp-connect.md)                 | Connecte le NPP au réseau.<br/>                                                                                        |
| [**Déconnecter**](iesp-disconnect.md)           | Déconnecte le NPP du réseau.<br/>                                                                                   |
| [**GetControlState**](iesp-getcontrolstate.md) | Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.<br/> |
| [**Suspendre**](iesp-pause.md)                     | Arrête temporairement la capture en cours.<br/>                                                                                  |
| [**QueryStations**](iesp-querystations.md)     | Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.<br/>                           |
| [**QueryStatus**](iesp-querystatus.md)         | Récupère l’état du NPP.<br/>                                                                                        |
| [**Sort**](iesp-resume.md)                   | Reprend une capture suspendue.<br/>                                                                                               |
| [**Démarrer**](iesp-start.md)                     | Démarre la capture et crée le fichier de capture.<br/>                                                                        |
| [**Arrêter**](iesp-stop.md)                       | Arrête la capture en cours.<br/>                                                                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

