---
description: Spécifie si le décodeur doit effectuer Lt-Rt pli vers le dessous.
ms.assetid: ce1dc4ea-4326-40ab-bb30-ff1a34f06d79
title: MFPKEY_WMADEC_LTRTOUTPUT, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f4a83d2529ce3b37282be35924b48288d4df45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114426"
---
# <a name="mfpkey_wmadec_ltrtoutput-property"></a>MFPKEY \_ WMADEC \_ LTRTOUTPUT, propriété

Spécifie si le décodeur doit effectuer Lt-Rt pli vers le dessous.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Si cette propriété a la valeur VARIANT \_ false et que la sortie est stéréo, le décodeur audio utilise le repli de canal simple. Si cette propriété a la valeur VARIANT \_ true, le décodeur audio effectue une repliage Lt-Rt (matrice) vers le bout de la chaîne stéréo, puis tout décodeur Dolby Surround peut être utilisé pour décoder le surround à matrice. Par exemple, le décodeur audio peut effectuer Lt-Rt repli sur le contenu 5,1 ou 7,1.

Cette propriété est prise en charge uniquement lorsque le décodeur agit comme un objet de média DirectX (DMO). Aucun pli d’un type quelconque n’est pris en charge lorsque le décodeur agit comme une transformation de Media Foundation (MFT).

Sur Windows Vista, si vous obtenez une interface **IPropertyStore** sur un décodeur audio, le décodeur agit comme une table MFT. Par conséquent, cette propriété ne peut pas être utilisée sur Windows Vista. Pour plus d’informations sur le moment où un décodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
