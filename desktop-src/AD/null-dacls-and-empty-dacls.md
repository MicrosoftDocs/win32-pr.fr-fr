---
title: DACL null et DACL vides (AD DS)
description: La présence d’une liste de contrôle d’accès discrétionnaire null dans l’attribut nTSecurityDescriptor d’un objet peut créer un risque de sécurité grave.
ms.assetid: 32b786d2-e676-4402-ad22-550de9289494
ms.tgt_platform: multiple
keywords:
- DACL null et listes DACL vides
- DACL AD, NULL et Empty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a41e03917c1190b7926eca11db038e2143bcb91d142e0617d143d4d80bb6e601
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185794"
---
# <a name="null-dacls-and-empty-dacls-ad-ds"></a>DACL null et DACL vides (AD DS)

La présence d’une liste de contrôle d’accès discrétionnaire null dans l’attribut [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor) d’un objet peut créer un risque de sécurité grave. Une liste DACL null accorde un accès complet à tout utilisateur qui la demande ; la vérification de sécurité normale n’est pas effectuée par rapport à l’objet. Une DACL NULL ne doit pas être confondue avec une liste DACL vide. Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune entrée de contrôle d’accès (ACE). Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.

Pour plus d’informations, consultez [DACL null et DACL vides](/windows/desktop/SecAuthZ/null-dacls-and-empty-dacls).

 

 