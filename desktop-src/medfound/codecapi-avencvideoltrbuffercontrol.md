---
description: Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: CODECAPI_AVEncVideoLTRBufferControl, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236280"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>CODECAPI \_ propriété AVEncVideoLTRBufferControl

Spécifie le nombre maximal de cadres de référence à long terme (LTR) contrôlés par l’application.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoLTRBufferControl**

## <a name="property-value"></a>Valeur de la propriété

La valeur de ce contrôle inclut deux champs, où chaque champ a 16 bits.




| Valeur | Signification | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Les premiers bits de champ</strong></dt><dt>[0.. 15]</dt></dl> | Nombre de cadres LTR contrôlés par l’application.<br /><strong>Encodeurs H. 264/AVC :</strong><br /> En supposant que la valeur est N et que N est une valeur différente de zéro, à chaque image de la base de connaissances, l’encodeur doit automatiquement marquer les frames qui suivent la trame de la base de connaissances (et inclure le cadre de la base de demande) comme des cadres LTR, à condition que les 3 des éléments suivants s’appliquent :<ul><li>Le cadre n’est pas déjà défini pour être marqué comme cadre de référence à long terme.</li><li>Le cadre est un cadre de couche de base. Par exemple, l’élément de syntaxe <strong>temporal_id</strong> égal à 0.</li><li>Le nombre de frames actuellement marqués comme LTR est inférieur à N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Deuxième bits de champ</strong></dt><dt>[16.. 31]</dt></dl> | Mode d’approbation du contrôle LTR.<br /><strong>Encodeurs H. 264/AVC :</strong><br /> 1 (confiance jusqu’à) signifie que l’encodeur peut utiliser un frame LTR, sauf si l’application l’invalide explicitement via le contrôle <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br /> Les autres valeurs ne sont pas valides et réservées pour une utilisation ultérieure.<br /> | 




 

## <a name="remarks"></a>Notes

Il s’agit d’une API statique.

La valeur par défaut doit être 0

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




