---
description: les auteurs de Package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Attribution d’un nom aux tables, propriétés et actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd26ab08bcada936bdcb9c87d10cb060c697689cec8978a1eae0d25ac5c0a2d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105079"
---
# <a name="naming-custom-tables-properties-and-actions"></a>Attribution d’un nom aux tables, propriétés et actions personnalisées

les auteurs de Package doivent s’assurer que les noms de toutes les tables, propriétés ou actions personnalisées définies dans leur package n’entrent pas en conflit avec les noms de tables, de propriétés ou d’actions standard qui sont natives au Windows Installer.

Les auteurs de packages doivent respecter les instructions suivantes pour les noms de table, de propriété ou d’action personnalisés.

-   Créez des noms pour les tables, les propriétés ou les actions personnalisées qui ont un préfixe qui identifie votre application.
-   N’utilisez jamais de nom avec MSI comme préfixe. à partir de Windows Installer 2,0, toutes les nouvelles propriétés, actions et tables natives Windows Installer reçoivent des noms préfixés par Msi. Ce préfixe ne respecte pas la casse, par exemple MsiNewInternalTable. Étant donné que le préfixe ne respecte pas la casse, les auteurs doivent éviter tous les cas du préfixe msi.

Pour plus d’informations, consultez [noms de tables](table-names.md).

 

 



