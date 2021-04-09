---
description: Liste DACL pour un nouvel objet
ms.assetid: ff1146d7-5229-4c75-9768-28c3fab5fcea
title: Liste DACL pour un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01d1ec8e92d4d56f977d4454b9a67df0a9bd489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114134"
---
# <a name="dacl-for-a-new-object"></a>Liste DACL pour un nouvel objet

Le système utilise l’algorithme suivant pour créer une liste DACL pour la plupart des types de nouveaux objets sécurisables :

1.  La liste DACL de l’objet est la liste DACL du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifié par le créateur de l’objet. Le système fusionne toutes les entrées du contrôle d’accès (ACE) pouvant être héritées dans la liste DACL spécifiée, sauf si le \_ \_ bit protégé de se DACL est défini dans les bits de contrôle du descripteur de sécurité
2.  Si le créateur ne spécifie pas de descripteur de sécurité, le système génère la liste DACL de l’objet à partir d’ACE pouvant être héritées.
3.  Si aucun descripteur de sécurité n’est spécifié et qu’il n’y a pas d’ACE pouvant être héritées, la DACL de l’objet est la liste DACL par défaut du jeton [*principal*](/windows/desktop/SecGloss/p-gly) ou d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) du créateur.
4.  S’il n’existe pas d’ACL spécifiée, héritée ou par défaut, le système crée l’objet sans DACL, ce qui permet à tout le monde d’accéder entièrement à l’objet.

Le système utilise un algorithme différent pour générer une liste DACL pour un nouvel objet Active Directory. Pour plus d’informations, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
