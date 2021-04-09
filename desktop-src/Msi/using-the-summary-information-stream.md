---
description: Cette section décrit les fonctions de l’API Windows Installer qui peuvent appeler les propriétés du flux d’informations résumées. Pour plus d’informations sur le flux d’informations de résumé et son fonctionnement avec les bases de données, consultez à propos du flux d’informations de résumé.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Utilisation du flux d’informations de synthèse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952046"
---
# <a name="using-the-summary-information-stream"></a>Utilisation du flux d’informations de synthèse

Cette section décrit les fonctions de l’API Windows Installer qui peuvent appeler les propriétés du flux d’informations résumées. Pour plus d’informations sur le flux d’informations de résumé et son fonctionnement avec les bases de données, consultez [à propos du flux d’informations de résumé](about-the-summary-information-stream.md).

-   Il est important de se souvenir que le programme d’installation contient différents types de bases de données, et que certaines propriétés du flux d’informations de résumé ont des significations différentes selon les bases de données. Pour plus d’informations, consultez [Description des propriétés récapitulatives](summary-property-descriptions.md).
-   Lorsqu’une base de données est ouverte comme sortie d’une autre base de données, le flux d’informations de synthèse de la base de données de sortie est en fait un miroir en lecture seule de la base de données d’origine et ne peut donc pas être modifié. En outre, elle ne sera pas conservée avec la base de données. Pour créer ou modifier les informations de résumé de la base de données de sortie, vous devez la fermer, puis la rouvrir.

Les étapes suivantes décrivent comment utiliser les fonctions de flux de données de Résumé :

**Pour utiliser les propriétés du flux d’informations de synthèse**

1.  Obtenez un descripteur de la base de données contenant le flux d’informations de synthèse en appelant la fonction [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) .
2.  Appelez la fonction [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) pour obtenir le nombre de propriétés existantes.
3.  Appelez la fonction [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) pour afficher une seule propriété d’informations récapitulatives.
4.  Appeler la fonction [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) pour définir une propriété unique
5.  Appelez la fonction [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) pour enregistrer la propriété informations de synthèse.
6.  Appelez la fonction [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) pour créer les informations de résumé d’une transformation existante.

[Orca.exe](orca-exe.md) et [Msiinfo.exe](msiinfo-exe.md) sont des outils qui peuvent être utilisés pour modifier ou afficher le flux d’informations de synthèse d’une base de données. Ces outils sont uniquement disponibles dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

Vous pouvez également accéder au flux d’informations de synthèse à l’aide des méthodes et propriétés suivantes de l' [interface Automation](automation-interface.md)Windows Installer.

-   [**SummaryInfo. Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo. Persist**](summaryinfo-persist.md)
-   [**Programme d’installation. SummaryInformation**](installer-summaryinformation.md)
-   [**Base de données. SummaryInformation**](database-summaryinformation.md)
-   [**Base de données. CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

Le WiSumInf.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md). Cet exemple de script peut être utilisé pour gérer le flux d’informations de synthèse d’un package de Windows Installer. Pour plus d’informations sur la WiSumInf.vbs, consultez [gérer les informations de résumé](manage-summary-information.md).

 

 



