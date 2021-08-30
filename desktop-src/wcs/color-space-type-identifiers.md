---
title: Identificateurs de types d’espace de couleurs
description: Ces constantes spécifient le type d’un tableau d’espace colorimétrique PostScript 2. Les valeurs suivantes sont des types de tableau d’espace colorimétrique valides.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 199348fc23282a104c66f153b5c1ea43027464e5aa2522db61c6658d3425bdc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007689"
---
# <a name="color-space-type-identifiers"></a>Identificateurs de types d’espace de couleurs

Ces constantes spécifient le type d’un tableau d’espace colorimétrique PostScript 2. Les valeurs suivantes sont des types de tableau d’espace colorimétrique valides.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace colorimétrique CIEBasedA à partir du profil monochrome.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_gris CSA**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace colorimétrique CIEBasedA à partir du profil monochrome.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace de couleurs CIEBasedABC à partir du profil RVB ou L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**\_définition CSA**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace de couleurs CIEBasedDEF à partir du profil RVB ou L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**\_RGB CSA**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace de couleurs CIEBasedDEF suivi d’un tableau d’espaces de couleurs CIEBasedABC à partir du profil RGB. À l’exécution, si l’imprimante ne prend pas en charge les espaces de couleurs CIEBasedDEF, la fonction utilise la définition CIEBasedABC.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratoire CSA**
</dt> <dd> <dl> <dt>



Obtient un tableau d’espaces de couleurs CIEBasedABC à partir du <sup>\*</sup> Profil L a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_DEFG CSA**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace colorimétrique CIEBasedDEFG à partir du profil CMJN.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**\_CMJN CSA**
</dt> <dd> <dl> <dt>



Obtenir un tableau d’espace colorimétrique CIEBasedCMYK à partir du profil CMJN.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[constantes ICM](wcs-constants.md)
</dt> </dl>

 

 




