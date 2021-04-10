---
title: Fournir une interface utilisateur
description: Fournir une interface utilisateur
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- Plug-ins du lecteur Windows Media, pages de propriétés
- plug-ins, pages de propriétés
- plug-ins de traitement de signal numérique, pages de propriétés
- Plug-ins DSP, pages de propriétés
- plug-ins de traitement de signal numérique, interface utilisateur
- Plug-ins DSP, interface utilisateur
- pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197182"
---
# <a name="providing-a-user-interface"></a>Fournir une interface utilisateur

Les plug-ins DSP peuvent fournir une page de propriétés pour créer une interface utilisateur. Pour ce faire, le plug-in doit inclure un objet page de propriétés qui fournit une implémentation d’une interface **IPropertyPage** . L’objet de plug-in DSP doit implémenter **ISpecifyPropertyPages :: GetPages**, qui permet au lecteur Windows Media de localiser et d’identifier la page de propriétés appropriée pour le plug-in.

**Affichage d’un graphique d’État**

Les plug-ins DSP peuvent afficher un petit graphique ou une série de graphiques dans la zone État du lecteur Windows Media pour informer l’utilisateur qu’un plug-in est actif. Pour prendre en charge cette fonctionnalité, le plug-in doit implémenter l’interface **IPropertyBag** . Le lecteur Windows Media appelle **IPropertyBag :: Read**, en fournissant un pointeur vers le nom de la propriété demandée « IconStreams », qui respecte la casse, et un pointeur vers une structure **Variant** qui reçoit les données du graphique. Le plug-in crée un objet **IStream** (ou un SAFEARRAY d’objets **IStream** s’il y a plusieurs graphiques), puis charge les données graphiques, y compris les informations d’en-tête, dans le flux, puis retourne un pointeur vers l’objet **IStream** à l’aide du membre **punkVal** de la structure **Variant** . Si le plug-in ne fournit qu’un graphique, il spécifie le membre **VT** de la structure **Variant** comme VT \_ inconnu. Si le plug-in fournit plusieurs objets Graphics **IStream** à l’aide d’un SafeArray, il spécifie le membre **VT** de la structure **Variant** en tant que \_ tableau VT.

Les graphiques peuvent être stockés dans différents formats de fichiers, notamment :

**BMP**

Les images bitmap Microsoft Windows ne sont pas compressées.

**JPEG**

Format d’image compressé couramment utilisé pour les pages Web. Les fichiers de format JPEG ont généralement des extensions de nom de fichier. jpg.

**FORMATS**

Format d’image compressé couramment utilisé pour les pages Web.

**FORMAT**

Format d’image compressé couramment utilisé pour les pages Web.

Les dimensions maximales pour les graphiques de plug-in DSP sont de 38 pixels de large et de 14 pixels de haut.

Le flux d’octets **IStream** contenant le graphique d’État doit inclure des informations d’en-tête. Sans informations d’en-tête, le lecteur Windows Media ne peut pas identifier correctement le type de graphique et, par conséquent, ne charge pas l’image.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




