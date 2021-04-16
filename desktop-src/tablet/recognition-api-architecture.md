---
description: Une application compatible avec l’encre communique avec le système de reconnaissance via les API de la plateforme Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Architecture de l’API de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104567149"
---
# <a name="recognition-api-architecture"></a>Architecture de l’API de reconnaissance

Une application compatible avec l’encre communique avec le système de reconnaissance via les API de la plateforme Tablet PC. Les applications utilisent l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) pour y parvenir. La plateforme Tablet PC interagit avec votre module de reconnaissance à l’aide des interfaces de style C documentées dans cette section. Dans l’illustration suivante, la zone à l’intérieur de la ligne en pointillés indique ce qui est documenté dans cette section.

![illustration de l’architecture de reconnaissance avec reconnaissance en surbrillance](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

Un module de reconnaissance personnalisé doit inclure Récapitulatifis. h (installé par défaut dans C : \\ Program Files \\ Microsoft Tablet PC Platform SDK \\ include). Sauf indication contraire, votre bibliothèque de liens dynamiques (DLL) doit exporter toutes les fonctions d’API, même si vous choisissez d’en faire une, vous devez retourner E \_ NOTIMPL.

En aucun cas, votre module de reconnaissance sera appelé directement par une application compatible avec l’écriture manuscrite. Au lieu de cela, les applications appellent les API d’automatisation ou les API gérées pour obtenir les résultats de votre module de reconnaissance.

 

 



