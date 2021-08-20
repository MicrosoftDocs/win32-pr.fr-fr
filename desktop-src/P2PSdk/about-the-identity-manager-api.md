---
description: L’API du gestionnaire d’identités homologues vous permet de créer, d’énumérer et de manipuler des identités d’homologue dans une application homologue.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: À propos du gestionnaire d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d062f7324bb949c657b7687b533058cb9e74d3102eea1e484284453d3ff7f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579919"
---
# <a name="about-identity-manager"></a>À propos du gestionnaire d’identité

L’API du gestionnaire d’identités homologues vous permet de créer, d’énumérer et de manipuler des identités d’homologue dans une application homologue. Vous pouvez utiliser les identités d’homologue créées à l’aide de cette API comme entrée pour le regroupement d’homologues et les API du fournisseur d’espace de noms PNRP (Peer Name Resolution Protocol).

## <a name="peer-identity-manager-best-practices"></a>Meilleures pratiques pour Peer Identity Manager

Chaque utilisateur doit avoir plusieurs identités d’homologue qu’il peut utiliser pour les activités homologues. Par exemple, un utilisateur peut avoir deux identités d’homologue pour le travail et le loisir.

Une application homologue bien conçue permet à un utilisateur de sélectionner une identité d’homologue à utiliser. Un utilisateur peut créer une nouvelle identité d’homologue si aucune des identités d’homologue existantes n’est appropriée pour une utilisation avec une application.

Une application homologue bien conçue contrôle également le nombre d’identités qu’elle crée. Si une application crée une identité d’homologue temporaire, l’application doit supprimer l’identité d’homologue lorsque l’identité n’est pas nécessaire. Si une application n’effectue pas cette opération de maintenance, le gestionnaire d’identité de l’homologue peut ne pas être en mesure de créer des identités d’homologue tant que certaines identités d’homologue n’ont pas été

 

 



