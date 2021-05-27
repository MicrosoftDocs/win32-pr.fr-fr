---
title: Échec du dessin D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Échec d’un appel de dessin par une cible de rendu
keywords:
- Erreur de dessin D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549964"
---
# <a name="d1109-draw-failure"></a>D1109 : échec du dessin

Un appel de dessin par une cible de rendu a échoué \[  \] . Balises \[ *: étiquette1*, *tag2* \] .

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*ressource*
</dt> <dd>

Adresse de la cible de rendu.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*: étiquette1*
</dt> <dd>

La première valeur de la balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

La deuxième valeur de balise (pour plus d’informations, consultez [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Niveau d’erreur | Avertissement |



 

## <a name="possible-causes"></a>Causes possibles

Un appel de dessin peut échouer pour de nombreuses raisons. Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Direct2D pour la méthode qui a échoué.

 

 