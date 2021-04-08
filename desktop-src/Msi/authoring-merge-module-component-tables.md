---
description: Une table de composants est requise dans chaque module de fusion.
ms.assetid: ef4a0678-bf6b-47c9-89e8-40e12da52d9b
title: Création de tables de composants de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46557541b3a6b89841fe3e26cef7c00e59dc3911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034407"
---
# <a name="authoring-merge-module-component-tables"></a>Création de tables de composants de module de fusion

Une [table de composants](component-table.md) est requise dans chaque module de fusion. Cette table contient un enregistrement pour chaque composant remis par le module de fusion au fichier. msi cible. Notez que chacun de ces composants doit également être spécifié dans la [table ModuleComponents](modulecomponents-table.md) décrite dans [création de tables ModuleComponents](authoring-modulecomponents-tables.md).

Utilisez la Convention d’affectation de noms standard lorsque vous entrez des noms dans la colonne composant pour vous assurer que l’identificateur de chaque composant est unique pour tous les modules de fusion et les bases de données d’installation. Pour plus d’informations, consultez [attribution de noms aux clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).

Renseignez les champs restants dans chaque enregistrement comme décrit pour une base de données d’installation dans la [table des composants](component-table.md). Les composants ajoutés à un package par un module de fusion doivent respecter les instructions relatives aux composants Windows Installer valides décrits dans les sections suivantes :

-   [Composants Windows Installer](windows-installer-components.md)
-   [Organisation des applications en composants](organizing-applications-into-components.md)

 

 



