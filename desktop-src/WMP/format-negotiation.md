---
title: Négociation de format
description: Négociation de format
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- plug-ins Lecteur Windows Media, négociation de format
- plug-ins, négociation de format
- plug-ins de traitement de signal numérique, négociation de format
- Plug-ins DSP, négociation de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69669bc3af82400ea62d154335d117fef185d0b34184be4101ffa5ae309e6ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054967"
---
# <a name="format-negotiation"></a>Négociation de format

pour Lecteur Windows Media et un plug-in DSP pour partager des données, les deux programmes doivent s’accorder sur le format des données qu’ils traitent. Le plug-in DSP implémente les méthodes que le lecteur appelle pour déterminer les formats pris en charge par le plug-in. Le plug-in implémente également des méthodes que le lecteur appelle pour définir le format actuel.

si le plug-in joue le rôle d’un objet multimédia DirextX (DMO), Lecteur Windows Media découvre et définit les formats multimédias en appelant les méthodes de l’interface **IMediaObject** . Par exemple, le lecteur appelle à plusieurs reprises le plug-in **IMediaObject :: GetInputType** pour obtenir une liste de tous les formats d’entrée pris en charge par le plug-in. les plug-ins DMO utilisent la structure de **\_ \_ TYPE de média DMO** pour organiser les informations qui spécifient un format de média. pour plus d’informations sur la façon dont les plug-ins DMO et le format negotiate du lecteur, consultez [à propos de IMediaObject](about-imediaobject.md).

si le plug-in agit en tant que Media Foundation Transform (MFT), Lecteur Windows Media découvre et définit les formats multimédias en appelant les méthodes de l’interface **IMFTransform** . Par exemple, le lecteur appelle à plusieurs reprises le plug-in **IMFTransform :: GetInputAvailableType** pour obtenir une liste de tous les formats d’entrée pris en charge par le plug-in. Les plug-ins MFT et le lecteur utilisent l’interface **IMFMediaType** pour organiser et échanger des informations de format.

Lecteur Windows Media utilisera un plug-in DSP audio uniquement si le plug-in prend en charge la même profondeur de bits que le son numérique en cours de lecture. Par exemple, si le son numérique est de 20 bits, le plug-in doit être écrit pour traiter le son 20 bits. Pour les CD audio, les plug-ins DSP doivent prendre en charge le traitement 20 bits.

lors de la négociation de format du contenu multicanaux sur un ordinateur configuré pour une utilisation avec des intervenants stéréo, Lecteur Windows Media tente d’abord de se connecter à un plug-in audio DSP à l’aide du format d’entrée et de sortie existant en appelant **IMediaObject :: SetInputType** et **IMediaObject :: SetOutputType**. Une fois cette négociation initiale effectuée, le lecteur énumère ensuite les formats pris en charge par le plug-in et tente de négocier la combinaison de format optimale pour le lecteur et le plug-in. Si le plug-in accepte l’audio stéréo (définie par une structure **WAVEFORMATEX** ) comme format d’entrée lors de la négociation initiale, puis accepte uniquement l’audio multicanaux (défini par une structure **WAVEFORMATEXTENSIBLE** ), le lecteur fournit un son de multicanaux comme format d’entrée au plug-in. ce comportement au cours de la négociation de format peut être utilisé dans le système d’exploitation Microsoft Windows XP. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




