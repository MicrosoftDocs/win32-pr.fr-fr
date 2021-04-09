---
description: WSPGetSockName est utilisé pour récupérer l’adresse locale pour les sockets liés.
ms.assetid: 5f3c9aa8-97fe-48a1-a3f5-156c9bddb1b2
title: Détermination des noms locaux et distants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 265cf8013dcadaedbef786ab78f48e63de81a992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033984"
---
# <a name="determining-local-and-remote-names"></a>Détermination des noms locaux et distants

[**WSPGetSockName**](/previous-versions/windows/desktop/legacy/ms742280(v=vs.85)) est utilisé pour récupérer l’adresse locale pour les sockets liés. Cela s’avère particulièrement utile lorsqu’un appel [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) a été effectué sans commencer par [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85)) . **WSPGetSockName** fournit le seul moyen de déterminer l’association locale qui a été définie implicitement par le fournisseur.

Une fois la connexion configurée, [**WSPGetPeerName**](/previous-versions/windows/desktop/legacy/ms742278(v=vs.85)) peut être utilisé pour déterminer l’adresse de l’homologue auquel un socket est connecté.

 

 
