---
description: Identification des opérations DVD valides
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identification des opérations DVD valides
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd1b99a38949ca0ff54d391e9ad5458bbe854a5c4af4140b15deaf4177147aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051979"
---
# <a name="identifying-valid-dvd-operations"></a>Identification des opérations DVD valides

Plusieurs facteurs déterminent si vous pouvez effectuer une opération DVD donnée :

-   Domaine actuel. Certaines commandes ne sont valides que dans certains domaines. Lorsque le domaine change, le navigateur envoie un \_ événement de modification de domaine de DVD EC \_ \_ . Vous pouvez également appeler [**IDvdInfo2 :: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) pour accéder au domaine actuel.
-   Indicateurs UOPS. Il s’agit d’indicateurs écrits sur le disque, indiquant les opérations autorisées. Chaque fois que les indicateurs changent, le navigateur envoie un \_ événement de modification UOPs de DVD ce DVD \_ \_ \_ avec les nouveaux indicateurs. Vous pouvez également appeler [**IDvdInfo2 :: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) pour récupérer les indicateurs UOPs actuels.
-   Contenu du DVD. Certaines commandes peuvent ne pas être pertinentes en fonction du contenu du DVD. Par exemple, la méthode [**IDvdControl2 :: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) peut être autorisée en fonction du domaine actuel et des indicateurs UOPs, mais la vidéo peut avoir un seul angle. Dans ce cas, l’appel **SelectAngle** est autorisé, mais n’est pas une option significative.

En cas de doute, autoriser une action. Au pire, la méthode [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) échoue et vous pouvez fournir des commentaires à l’utilisateur. Les commentaires doivent être relativement discrets. Par exemple, vous pouvez faire clignoter un petit X rouge pour alerter l’utilisateur. Le navigateur DVD retourne VFW \_ e \_ DVD \_ INVALIDDOMAIN lorsque le domaine interdit une opération, et que le \_ fonctionnement du DVD VFW e est \_ \_ \_ bloqué lorsque les indicateurs UOPs interdisent une opération.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> </dl>

 

 



