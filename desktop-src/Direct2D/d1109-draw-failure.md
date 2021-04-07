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
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730077"
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

|             |         |
|-------------|---------|
| Niveau d’erreur | Avertissement |



 

## <a name="possible-causes"></a>Causes possibles

Un appel de dessin peut échouer pour de nombreuses raisons. Pour plus d’informations, consultez la documentation du kit de développement logiciel (SDK) Direct2D pour la méthode qui a échoué.

 

 