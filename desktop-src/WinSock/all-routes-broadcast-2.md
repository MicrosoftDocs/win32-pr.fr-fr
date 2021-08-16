---
description: Une diffusion générale via Internet est obtenue en définissant les \_ champs sa netnum et sa \_ nodeNum sur Binary (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Diffusion de tous les itinéraires
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322719"
---
# <a name="all-routes-broadcast"></a>Diffusion de tous les itinéraires

Une diffusion générale via Internet est obtenue en définissant les champs **sa \_ netnum** et **sa \_ nodeNum** sur Binary (1). Le fournisseur de services traduit cette requête en un paquet type-20, que les routeurs IPX reconnaissent et transfèrent. Le paquet visite tous les sous-réseaux et peut être dupliqué plusieurs fois. Les destinataires doivent gérer plusieurs copies dupliquées du datagramme.

L’utilisation de ce type de diffusion n’est pas populaire parmi les administrateurs réseau. son utilisation doit donc être extrêmement limitée. De nombreux routeurs désactivent ce type de diffusion, laissant les parties du sous-réseau invisible au paquet.

 

 



