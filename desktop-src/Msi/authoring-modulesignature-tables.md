---
description: La table ModuleSignature contient toutes les informations nécessaires pour identifier le module de fusion.
ms.assetid: 5f0b4590-dac3-4528-b714-ff760ae8d123
title: Création de tables ModuleSignature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796775b0237c17db4fa21075a792c372bed3e97b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518651"
---
# <a name="authoring-modulesignature-tables"></a>Création de tables ModuleSignature

La [table ModuleSignature](modulesignature-table.md) contient toutes les informations nécessaires pour identifier le module de fusion.

Le champ ModuleID est la clé primaire de cette table et doit respecter la convention décrite dans [nommage des clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md). Par exemple, si le nom lisible du module de fusion est MyLibrary et que le GUID du module de fusion est {880DE2F0-CDD8-11D1-A849-006097ABDE17}, l’entrée dans la colonne ModuleID de la table ModuleSignature devient MyLibrary. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.

Entrez l’identificateur décimal pour la langue par défaut du module de fusion dans le champ Language de la table ModuleSignature.

Entrez la version du module de fusion dans le champ version.

 

 



