---
title: Choix d’un niveau d’authentification
description: Lors du choix d’un niveau d’authentification, utilisez les instructions suivantes.
ms.assetid: 6efb4162-5884-4bcb-86da-4809f89f0c26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ba73b2541497ff70204151e57f0483ac7965ef2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462162"
---
# <a name="choosing-an-authentication-level"></a>Choix d’un niveau d’authentification

Lors du choix d’un niveau d’authentification, utilisez les instructions suivantes. S’il n’est pas important que les données envoyées puissent être interceptées et modifiées, et que les données reçues puissent être interceptées ou modifiées, utilisez \_ le niveau d’authentification RPC C « \_ \_ aucun » \_ , qui est la valeur par défaut. Si les données ne doivent pas être modifiées et que les données privées ne sont pas envoyées ou reçues, \_ Utilisez \_ \_ \_ l’intégrité PKT du niveau d’authentification RPC C \_ . Dans tous les autres cas, utilisez \_ la \_ confidentialité du niveau d’authentification RPC C \_ \_ \_ .

N’utilisez pas le \_ niveau d’authentification RPC c \_ \_ par défaut, le niveau d' \_ \_ authentification RPC c \_ \_ Connect, l’appel de niveau d’authentification \_ RPC \_ c ou le \_ niveau d' \_ authentification par \_ \_ authentification c RPC \_ \_ \_ . Une personne malveillante sophistiquée peut arrêter ces niveaux d’authentification et les rendre inefficaces. Chacun de ces niveaux rend légèrement plus difficile pour une personne malveillante d’intercepter et de modifier des données, et d’emprunter l’identité, mais la sécurité n’est pas vraiment obtenue. Étant donné que le niveau de sophistication d’une personne malveillante est rarement connu, il ne s’agit pas de choix judicieux.

 

 




