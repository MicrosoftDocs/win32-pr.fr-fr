---
description: SACL pour un nouvel objet
ms.assetid: 1d0d6fee-e5ec-4d8f-8ed8-10c725c57a6a
title: SACL pour un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f9833fcfb45a612b6135579e44aca6f219661fd2aeb2998b899e5794fa7bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413839"
---
# <a name="sacl-for-a-new-object"></a>SACL pour un nouvel objet

Le système utilise l’algorithme suivant pour créer une liste SACL pour la plupart des types de nouveaux objets sécurisables :

1.  La liste SACL de l’objet est la liste SACL du [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) spécifié par le créateur de l’objet. le système fusionne les ace pouvant être héritées dans la liste sacl spécifiée, sauf si le \_ \_ bit protégé par le SE sacl est défini dans les bits de contrôle du descripteur de sécurité. \_ \_ \_ les ace d’attribut de ressource système et \_ \_ \_ \_ les ace d’ID de stratégie système d’un objet parent sont fusionnées dans un nouvel objet, même si le \_ bit protégé par le SE SACL \_ est défini.
2.  Si le créateur ne spécifie pas de descripteur de sécurité, le système génère la liste SACL de l’objet à partir d’ACE pouvant être héritées.
3.  S’il n’existe aucune SACL spécifiée ou héritée, l’objet n’a pas de SACL.

pour spécifier une liste SACL pour un nouvel objet, le créateur de l’objet doit avoir le \_ privilège SE nom de sécurité \_ activé. [](privileges.md) si la liste SACL spécifiée pour un nouvel objet contient uniquement des \_ ace d’attribut de ressource système \_ \_ , le \_ privilège de nom de sécurité SE \_ n’est pas obligatoire. Le créateur n’a pas besoin de ce privilège si la liste SACL de l’objet est générée à partir d’entrées de du même auteur.

Le système utilise un algorithme différent pour générer une liste SACL pour un nouvel objet Active Directory. Pour plus d’informations, voir [Comment les descripteurs de sécurité sont définis sur les nouveaux objets d’annuaire](/windows/desktop/AD/how-security-descriptors-are-set-on-new-directory-objects).

 

 
