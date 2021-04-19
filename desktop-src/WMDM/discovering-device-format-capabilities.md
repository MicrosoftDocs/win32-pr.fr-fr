---
title: Découverte des fonctionnalités de format des appareils
description: Découverte des fonctionnalités de format des appareils
ms.assetid: dd139816-dc8c-4e73-9a21-67287bfe6405
keywords:
- Gestionnaire de périphériques Windows Media, fonctionnalités de l’appareil
- Gestionnaire de périphériques, fonctionnalités de l’appareil
- Guide de programmation, fonctionnalités de l’appareil
- applications de bureau, fonctionnalités de l’appareil
- création d’applications Windows Media Gestionnaire de périphériques, fonctionnalités de l’appareil
- écriture de fichiers sur des appareils, fonctionnalités de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0ee05476f6b84bc85bb81cc7cff5815649f5842
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509995"
---
# <a name="discovering-device-format-capabilities"></a>Découverte des fonctionnalités de format des appareils

Votre application peut tenter de déterminer les fonctionnalités de lecture d’un appareil avant de lui envoyer un fichier. Si un appareil ne peut pas gérer le format d’un fichier que vous souhaitez envoyer, votre application peut tenter de Transcoder le fichier dans un format que l’appareil peut utiliser, ou informer l’utilisateur que l’appareil ne peut pas prendre en charge le fichier demandé.

Notez que certains périphériques, tels que les périphériques de classe de stockage de masse, peuvent servir uniquement de supports de stockage amovibles sans capacités de lecture. Dans ce cas, il serait inapproprié pour votre application de transcoder un fichier avant de l’envoyer à l’appareil.

Bien que la méthode [**IWMDMDevice :: GetType**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-gettype) permette à un appareil de signaler ses fonctionnalités, certains appareils retournent des valeurs incorrectes pour cette méthode. Avant de copier un fichier sur un appareil, vous souhaiterez peut-être demander à l’utilisateur si la lecture est prévue et, le cas échéant, tenter de Transcoder le fichier dans l’un des formats signalés de l’appareil (ou un format raisonnable, si l’appareil réclame une prise en charge de n’importe quel format). Une autre approche consiste à supposer que tous les formats spécifiquement répertoriés comme pris en charge par l’appareil sont destinés à la lecture, et que tous les autres fichiers doivent être transférés sans modification.

Après avoir découvert le format du fichier à transférer et les formats pris en charge par un appareil, vous pouvez choisir celui qui est le meilleur format cible pour le transcodage.

Dans le passé, il était courant pour une application de retourner zéro pour une propriété afin d’indiquer la prise en charge de toutes les valeurs de cette propriété. Par exemple, la valeur zéro pour [**\_ WAVEFORMATEX**](-waveformatex.md). nSamplesPerSec indique la prise en charge de n’importe quelle vitesse de transmission. À présent, la méthode recommandée pour indiquer la prise en charge de n’importe quelle valeur est de spécifier \_ \_ \_ les valeurs valides de WMDM enum prop \_ \_ dans [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md). ValidValuesForm. Toutefois, certaines propriétés peuvent retourner légitimement zéro pour indiquer une prise en charge spécifique. Par exemple, si [**\_ BITMAPINFOHEADER**](-bitmapinfoheader.md). biSizeImage est défini sur zéro, cela indique une \_ bitmap RGB bi. Les exceptions pour les valeurs zéro sont indiquées dans la documentation pour les structures pertinentes.

Toutefois, il est important de noter que les appareils ne signalent pas correctement leurs fonctionnalités de format ou de manière standard. Par exemple, les appareils signalent souvent qu’ils prennent en charge n’importe quel format, en fait, ils peuvent uniquement gérer des formats spécifiques, ou des vitesses de bits spécifiques au sein d’un type de format. C’est à vous de décider si votre application doit accepter ces rapports, ou si elle doit supposer un type de limite supérieure aux capacités de lecture d’un appareil (par exemple, 192 Kbits/s).

La méthode recommandée pour demander la prise en charge du format d’un appareil est [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability). Si cette méthode n’est pas prise en charge, votre application doit revenir à [**IWMDMDevice :: GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getformatsupport). **GetFormatSupport**, contrairement à **GetFormatSupport2**, ne retourne pas d’informations vidéo.

La façon dont une application demande les capacités de format d’un appareil dépend de l’interface prise en charge par l’application. Pour plus de détails, consultez les rubriques suivantes :

-   [Obtention des fonctionnalités de format sur les appareils qui prennent en charge IWMDMDevice3](getting-format-capabilities-on-devices-that-support-iwmdmdevice3.md)
-   [Obtention des fonctionnalités de format sur les appareils qui prennent en charge uniquement IWMDMDevice](getting-format-capabilities-on-devices-that-support-only-iwmdmdevice.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture de fichiers sur l’appareil**](writing-files-to-the-device.md)
</dt> </dl>

 

 




