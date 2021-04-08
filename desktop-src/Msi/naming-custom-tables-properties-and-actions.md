---
description: Les auteurs de package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Attribution d’un nom aux tables, propriétés et actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864082"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Attribution d’un nom aux tables, propriétés et actions personnalisées

Les auteurs de package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.

Les auteurs de packages doivent respecter les instructions suivantes pour les noms de table, de propriété ou d’action personnalisés.

-   Créez des noms pour les tables, les propriétés ou les actions personnalisées qui ont un préfixe qui identifie votre application.
-   N’utilisez jamais de nom avec MSI comme préfixe. À partir de Windows Installer 2,0, toutes les nouvelles propriétés, actions et tables natives Windows Installer reçoivent des noms préfixés par MSI. Ce préfixe ne respecte pas la casse, par exemple MsiNewInternalTable. Étant donné que le préfixe ne respecte pas la casse, les auteurs doivent éviter tous les cas du préfixe msi.

Pour plus d’informations, consultez [noms de tables](table-names.md).

 

 



