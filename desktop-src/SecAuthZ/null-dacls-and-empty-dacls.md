---
description: Une liste DACL null accorde un accès complet à tous les utilisateurs qui le demandent. Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune entrée de contrôle d’accès. Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACL null et DACL vides (autorisation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907819"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACL null et DACL vides (autorisation)

Si la [*liste de contrôle d’accès discrétionnaire (DACL, Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) qui appartient au [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) d’un objet a la valeur **null**, une DACL null est créée. Une liste DACL null accorde un accès complet à tout utilisateur qui la demande ; la vérification de sécurité normale n’est pas effectuée par rapport à l’objet. Une DACL NULL ne doit pas être confondue avec une liste DACL vide. Une liste DACL vide est une liste DACL correctement allouée et initialisée qui ne contient aucune [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE). Une liste DACL vide n’accorde aucun accès à l’objet auquel elle est assignée.

Pour obtenir un exemple de création d’une liste DACL, consultez [création d’une liste DACL](/windows/desktop/SecBP/creating-a-dacl).

 

 
