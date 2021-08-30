---
title: Déclaration de la fonctionnalité de l’appareil
description: Cette rubrique explique comment déclarer le GUID des fonctionnalités de l’appareil.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: d26d41c0f011c21f9f454651adec976a559bdbe20dd75f291404efcd30f2bb5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029079"
---
# <a name="declaring-the-device-capability"></a>Déclaration de la fonctionnalité de l’appareil

Cette rubrique explique comment déclarer le GUID des fonctionnalités de l’appareil. Toutes les applications qui ciblent des pilotes personnalisés doivent déclarer cette fonctionnalité.

Dans votre manifeste d’application, vous devez ajouter une fonctionnalité de périphérique, comme suit :

Il s’agit d’un exemple de déclaration de fonctionnalité pour un appareil personnalisé. Le GUID est le GUID de la classe d’interface de l’appareil.

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a>Rubriques connexes

[exemple d’accès personnalisé aux pilotes](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [applications de l’appareil UWP pour les appareils internes](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Centre de développement matériel](/windows-hardware/drivers/)
