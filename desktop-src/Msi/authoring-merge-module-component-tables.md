---
description: Une table de composants est requise dans chaque module de fusion.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Création de tables de composants de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 728fa03b7041933aff5fc00d839979d90e634853efde1d369970c116367b4637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264019"
---
# <a name="authoring-merge-module-component-tables"></a>Création de tables de composants de module de fusion

Une [table de composants](component-table.md) est requise dans chaque module de fusion. Cette table contient un enregistrement pour chaque composant remis par le module de fusion au fichier de .msi cible. Notez que chacun de ces composants doit également être spécifié dans la [table ModuleComponents](modulecomponents-table.md) décrite dans [création de tables ModuleComponents](authoring-modulecomponents-tables.md).

Utilisez la Convention d’affectation de noms standard lorsque vous entrez des noms dans la colonne composant pour vous assurer que l’identificateur de chaque composant est unique pour tous les modules de fusion et les bases de données d’installation. Pour plus d’informations, consultez [attribution de noms aux clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).

Renseignez les champs restants dans chaque enregistrement comme décrit pour une base de données d’installation dans la [table des composants](component-table.md). les composants ajoutés à un package par un module de fusion doivent respecter les instructions relatives aux composants Windows Installer valides décrits dans les sections suivantes :

-   [Windows Composants du programme d’installation](windows-installer-components.md)
-   [Organisation des applications en composants](organizing-applications-into-components.md)

 

 



