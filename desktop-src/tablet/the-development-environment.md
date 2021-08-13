---
description: Vous n’avez pas besoin d’un Tablet PC pour développer des applications Tablet PC, mais vous avez besoin d’un ordinateur personnel qui peut exécuter les logiciels listés plus loin dans cette rubrique.
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: L’environnement de développement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6d6c0de35fa84ec4ee01b3f25aaefec6ab3470fde83161f7aaf2157197bbf1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449212"
---
# <a name="the-development-environment"></a>L’environnement de développement

Vous n’avez pas besoin d’un Tablet PC pour développer des applications Tablet PC, mais vous avez besoin d’un ordinateur personnel qui peut exécuter les logiciels listés plus loin dans cette rubrique.

Nous vous recommandons vivement de tester votre application sur un Tablet PC réel pour vous assurer que toutes les différences de matériel, telles que le digitaliseur de résolution supérieur, sont comptabilisées.

Un système de développement minimal standard est constitué du matériel et des logiciels suivants.

## <a name="hardware"></a>Matériel

-   8 Mo d’espace disque dur pour une installation complète.
-   Un dispositif de pointage pour l’entrée. Cela comprend les appareils tels qu’une souris, une tablette externe ou un Tablet PC avec un digitaliseur HID.

HID est l’acronyme de Human Interface Device, une norme pour les périphériques d’entrée. Les numériseurs non conformes à HID sont traités comme une souris normale, tandis que les numériseurs conformes aux HID ont une résolution plus élevée et davantage de métadonnées sur les traits, tels que la pression, similaires à ceux installés sur le matériel Tablet PC.

## <a name="software"></a>Logiciel

Les systèmes d’exploitation suivants peuvent être utilisés pour développer des applications Tablet PC :

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Édition Tablet PC 2005
-   Windows Server 2003
-   Windows XP Professionnel

Vous aurez également besoin des éléments suivants :

-   Visual Studio version 6 avec Service Pack 5 ou Visual Studio .net, ou Visual Studio .net 2005
-   Microsoft Internet Explorer 6 ou version ultérieure (recommandé)

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>Détails sur le développement sur des références SKU non-Tablet PC de Windows

les composants de la plateforme Tablet PC peuvent être installés sur Windows XP Professional avec Service Pack 2 ou Windows Server 2003. Sur ces systèmes d’exploitation, votre application peut collecter de l’encre avec la classe [**InkCollector**](inkcollector-class.md) et peut être testée et déboguée. toutefois, aucune reconnaissance n’est disponible, sauf si vous installez également le Pack de reconnaissance 2005 de Microsoft Windows XP Tablet PC Edition. Vous pouvez télécharger ce pack à partir du centre de téléchargement sur MSDN.

après l’installation de l’SDK Windows sur un système Windows XP Professional ou Windows Server 2003, vous disposerez de tous les fichiers de développement nécessaires pour générer des applications manuscrites (telles que msinkaut. h pour un développeur COM). Toutefois, vous ne pourrez pas exécuter ou déboguer votre application sur ce système tant que vous n’aurez pas installé les fichiers du Runtime. Par exemple, dans le cas d’un développeur COM, inkobj.dll doit être installé et inscrit. Étant donné que vous n’êtes pas sur un système où ces fichiers de plateforme existent, vous devez installer les composants de plateforme Tablet PC à partir du module de fusion redistribuable, mstpcrt. msm, pour obtenir les fichiers du Runtime sur votre système.

la façon la plus simple d’obtenir les runtimes de plateforme installés sur un système Windows XP Professional ou Windows 2000 à des fins de développement est de compiler l’exemple de projet d’installation fourni avec les exemples d’ordinateurs portables et de Tablet pc et de les déployer sur l’ordinateur de développement.

> [!Note]  
> Windows Vista et Windows XP édition Tablet pc 2005 disposent déjà des composants de plateforme installés. ils ne nécessitent donc pas d’étapes supplémentaires pour exécuter et déboguer des applications Tablet pc.

 

les contrôles [InkEdit](inkedit-control-reference.md) et [InkPicture](inkpicture-control-reference.md) peuvent être utilisés pour collecter l’encre sur Windows 2000 avec service pack 4 ou Windows XP Professional avec service pack 2 lorsque les composants de plateforme tablet pc sont présents en installant le kit de développement logiciel (SDK) tablet pc version 1,7, mais ne peuvent pas collecter l’encre sur les systèmes non-tablet pc sur lesquels les composants de plateforme tablet pc ne sont pas installés.

le SDK Windows fournit tous les composants nécessaires pour développer des applications Tablet PC sur des références (sku) non-tablettes de Windows. Définissez la clé de Registre **DWORD** suivante sur 1 pour collecter l’encre sur les références (SKU) non-tablette de Windows :

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

Cette clé est conçue uniquement à des fins de développement.

 

 



