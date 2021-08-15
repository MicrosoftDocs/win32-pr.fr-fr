---
description: Compatibilité du schéma CIM
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: Compatibilité du schéma CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d87f1e40a52998f3a53a9b06f0572d8916b4a53663354ca5ffde67beaeed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319785"
---
# <a name="cim-schema-compatibility"></a>Compatibilité du schéma CIM

un composant clé de l’infrastructure Windows Management Instrumentation (WMI) est un modèle orienté objet des entités gérables dans un système. Le modèle est conforme à un standard géré par la[DMTF](https://www.dmtf.org/standards/wsman)(Desktop Management Task Force) et est connu comme le Common Information Model (CIM). Le schéma CIM fournit un mécanisme de description de données unique pour toutes les données qu’ils fournissent.

à partir de Windows 7, WMI est compatible avec la version de schéma CIM 2.17.1 ( [https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171) ). les utilisateurs peuvent maintenant compiler un schéma DMTF défini sur un ordinateur Windows.

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>Avantages de la compatibilité de la version de schéma CIM 2.17.1

-   lorsqu’un utilisateur télécharge des fichiers de schéma CIM version 2.17.1 ou DMTF, ceux-ci peuvent être compilés correctement sur l’ordinateur Windows cible.
-   La version de schéma CIM 2.17.1 a ajouté la prise en charge du BIOS, des imprimantes, des messages standard, de l’état du système d’exploitation, des paradigmes de gestion de l’alimentation modernes, de la virtualisation et de la sécurité.
-   La version de schéma CIM 2.1.7.1 offre une prise en charge de profil supplémentaire. Pour plus d’informations, consultez [Cross namespace Association Traversal](cross-namespace-association-traversal.md)

 

 



