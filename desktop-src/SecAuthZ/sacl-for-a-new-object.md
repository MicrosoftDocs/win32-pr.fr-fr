---
description: SACL pour un nouvel objet
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL pour un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb5bb5f276a869da3f48776bf96379edbd4af1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544703"
---
# <a name="sacl-for-a-new-object"></a>SACL pour un nouvel objet

Le système utilise l’algorithme suivant pour créer une liste SACL pour la plupart des types de nouveaux objets sécurisables :

1.  La liste SACL de l’objet est la liste SACL du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifié par le créateur de l’objet. Le système fusionne les ACE pouvant être héritées dans la liste SACL spécifiée, sauf si le \_ \_ bit protégé par la se est défini dans les bits de contrôle du descripteur de sécurité. \_ \_ \_ Les ACE d’attribut de ressource système et \_ \_ \_ \_ les ACE d’ID de stratégie système d’un objet parent sont fusionnées dans un nouvel objet, même si le bit protégé par le système d’application système \_ \_ est défini.
2.  Si le créateur ne spécifie pas de descripteur de sécurité, le système génère la liste SACL de l’objet à partir d’ACE pouvant être héritées.
3.  S’il n’existe aucune SACL spécifiée ou héritée, l’objet n’a pas de SACL.

Pour spécifier une liste SACL pour un nouvel objet, le créateur de l’objet doit avoir \_ le \_ [privilège](privileges.md) nom de sécurité se activé. Si la liste SACL spécifiée pour un nouvel objet contient uniquement des \_ ACE d’attribut de ressource système \_ \_ , le \_ privilège de nom de sécurité se \_ n’est pas obligatoire. Le créateur n’a pas besoin de ce privilège si la liste SACL de l’objet est générée à partir d’entrées de du même auteur.

Le système utilise un algorithme différent pour générer une liste SACL pour un nouvel objet Active Directory. Pour plus d’informations, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
