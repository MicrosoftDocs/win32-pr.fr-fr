---
description: La règle générale est qu’une application de bureau peut appeler une API Windows Runtime (WinRT). Toutefois, certaines API, y compris les API d’interface utilisateur XAML, requièrent que l’application appelante ait une identité de package.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT pouvant être appelées à partir d’une application de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9083fbfb16391c626f49b79176fed7a81068c028
ms.sourcegitcommit: 0c786b1682063d0cae0fc43180945183fa2c7981
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/24/2020
ms.locfileid: "104032083"
---
# <a name="calling-winrt-apis-from-a-desktop-app"></a>Appel d’API WinRT à partir d’une application de bureau

La règle générale est qu’une application de bureau peut appeler une API WinRT. Toutefois, certaines API, y compris les API d’interface utilisateur XAML, requièrent que l’application appelante ait une identité de package. Les applications UWP ont un modèle d’application bien défini, et elles ont une identité de package. Les autres types d’applications de bureau ne disposent pas d’un modèle d’application bien défini, ni d’une identité de package. Par conséquent, si une API requiert une identité de package, une application WPF, Windows Forms ou Win32 ne peut pas l’appeler, sauf si l’application [est empaquetée dans un package MSIX](/windows/msix/desktop/desktop-to-uwp-root).

## <a name="the-dualapipartition-attribute"></a>Attribut DualApiPartition

Il s’agit du processus à suivre chaque fois qu’un WinRT particulier que vous aimeriez appeler à partir de votre application de bureau. Ce processus répond à la question de savoir si l’API est autorisée à être appelée à partir d’une application de bureau. Tout d’abord, visitez les informations de référence sur l' [API Windows pour Windows Runtime Apps](/uwp/), recherchez la rubrique de référence pour l’API de classe ou de membre qui vous intéresse et vérifiez si l’attribut [**DualApiPartition**](/uwp/api/Windows.Foundation.Metadata.DualApiPartitionAttribute) est listé dans la section attributs.

## <a name="if-the-dualapipartition-attribute-is-listed"></a>Si l’attribut DualApiPartition est listé

Si l’attribut DualApiPartition est listé, l’API n’a pas besoin de l’application appelante pour avoir une identité de package, et l’API est autorisée à être appelée à partir de n’importe quelle application de bureau. [**Windows. Devices. géolocalisation. géolocator**](/uwp/api/Windows.Devices.Geolocation.Geolocator) est un exemple. une application n’a pas besoin d’être identifiée de manière unique afin d’effectuer des tâches d’emplacement.

## <a name="if-the-dualapipartition-attribute-is-not-listed"></a>Si l’attribut DualApiPartition n’est pas listé

Si l’attribut DualApiPartition n’est pas listé, l’API a besoin que l’application appelante ait une identité de package. Par conséquent, une application WPF, Windows Forms ou Win32 n’est pas autorisée à appeler l’API, sauf si l’application a été convertie en application UWP. [**Windows. UI. Xaml. Controls. Button**](/uwp/api/Windows.UI.Xaml.Controls.Button) est un exemple.
