---
title: Fournir une interface utilisateur
description: Fournir une interface utilisateur
ms.assetid: 43a0cfea-4f35-4c4a-97f5-a3787b597dc5
keywords:
- plug-ins Lecteur Windows Media, pages de propriétés
- plug-ins, pages de propriétés
- plug-ins de traitement de signal numérique, pages de propriétés
- Plug-ins DSP, pages de propriétés
- plug-ins de traitement de signal numérique, interface utilisateur
- Plug-ins DSP, interface utilisateur
- pages de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d708d1256faf7096d15a7596a9635a33173d22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013237"
---
# <a name="providing-a-user-interface"></a>Fournir une interface utilisateur

Les plug-ins DSP peuvent fournir une page de propriétés pour créer une interface utilisateur. Pour ce faire, le plug-in doit inclure un objet page de propriétés qui fournit une implémentation d’une interface **IPropertyPage** . l’objet de plug-in DSP doit implémenter **ISpecifyPropertyPages :: GetPages**, qui permet à Lecteur Windows Media de localiser et d’identifier la page de propriétés appropriée pour le plug-in.

**Affichage d’un graphique d’État**

les plug-ins DSP peuvent afficher un petit graphique ou une série de graphiques dans la zone d’état Lecteur Windows Media pour informer l’utilisateur qu’un plug-in est actif. Pour prendre en charge cette fonctionnalité, le plug-in doit implémenter l’interface **IPropertyBag** . Lecteur Windows Media appelle **IPropertyBag :: Read**, en fournissant un pointeur vers le nom de la propriété demandée « IconStreams », qui respecte la casse, et un pointeur vers une structure **VARIANT** qui reçoit les données du graphique. Le plug-in crée un objet **IStream** (ou un SAFEARRAY d’objets **IStream** s’il y a plusieurs graphiques), puis charge les données graphiques, y compris les informations d’en-tête, dans le flux, puis retourne un pointeur vers l’objet **IStream** à l’aide du membre **punkVal** de la structure **Variant** . Si le plug-in ne fournit qu’un graphique, il spécifie le membre **VT** de la structure **Variant** comme VT \_ inconnu. Si le plug-in fournit plusieurs objets Graphics **IStream** à l’aide d’un SafeArray, il spécifie le membre **VT** de la structure **Variant** en tant que \_ tableau VT.

Les graphiques peuvent être stockés dans différents formats de fichiers, notamment :

**AFFICHÉ**

les images Bitmap Microsoft Windows sont décompressées.

**GIF**

Format d’image compressé couramment utilisé pour les pages Web. Les fichiers de format JPEG ont généralement des extensions de nom de fichier .jpg.

**FORMATS**

Format d’image compressé couramment utilisé pour les pages Web.

**FORMAT**

Format d’image compressé couramment utilisé pour les pages Web.

Les dimensions maximales pour les graphiques de plug-in DSP sont de 38 pixels de large et de 14 pixels de haut.

Le flux d’octets **IStream** contenant le graphique d’État doit inclure des informations d’en-tête. sans informations d’en-tête, Lecteur Windows Media ne peut pas identifier correctement le type de graphique et, par conséquent, ne chargera pas l’image.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Vue d’ensemble des développeurs de plug-ins DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




