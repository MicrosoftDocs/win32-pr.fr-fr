---
description: L’API du fournisseur réseau spécifie une fonction de fonctions unique.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Fonctions fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141272"
---
# <a name="capabilities-functions"></a>Fonctions fonctions

L’API du fournisseur réseau spécifie une fonction de fonctions unique. Lorsque le système d’exploitation demande des informations sur les fonctionnalités d’un fournisseur de réseau, le [*routeur de fournisseur multiple*](/windows/desktop/SecGloss/m-gly) (MPR) appelle la fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) de chaque fournisseur réseau dont le réseau est actif.

La fonction [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) renvoie un masque de masque indiquant les fonctions de l’API du fournisseur réseau prises en charge par le fournisseur réseau. La fonction **NPGetCaps** est la seule fonction qu’un fournisseur réseau doit implémenter. Le système d’exploitation appelle cette fonction pour déterminer les autres fonctions de l’API du fournisseur réseau prises en charge par le fournisseur.

 

 
