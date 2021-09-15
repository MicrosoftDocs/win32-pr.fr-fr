---
description: Active Directory est le service d’annuaire pour Windows et constitue la base des réseaux distribués Windows.
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: Accès Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403771"
---
# <a name="accessing-active-directory"></a>Accès Active Directory

Active Directory est le service d’annuaire pour Windows et constitue la base des réseaux distribués Windows. Vous pouvez utiliser Active Directory pour localiser des objets dans un domaine réseau d’ordinateurs, tels que des utilisateurs, des stratégies de sécurité, des imprimantes, des composants distribués et d’autres ressources. Le nom Active Directory fait référence à la fois au service d’annuaire et au répertoire lui-même.

> [!Note]  
> Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).

 

Windows rend Active Directory accessible via WMI en créant un ensemble de références à chaque classe et objet contenu dans Active Directory. En accédant au fournisseur de services d’annuaire par le biais de WMI, vous pouvez créer des applications compatibles WMI qui peuvent accéder à la richesse des informations contenues dans Active Directory.

Avec ces interfaces, vous pouvez :

-   Récupérer des classes et des instances.
-   Énumérez les classes et les instances.
-   Créer des instances.
-   Modifiez des instances existantes.
-   Supprimer des instances existantes.
-   Active Directory de requête.

Les rubriques suivantes peuvent vous aider à utiliser Active Directory avec WMI :

-   [Utilisation de la syntaxe de Active Directory appropriée](using-the-proper-active-directory-syntax.md)
-   [Mappage de Active Directory à WMI](mapping-active-directory-to-wmi.md)

 

 



