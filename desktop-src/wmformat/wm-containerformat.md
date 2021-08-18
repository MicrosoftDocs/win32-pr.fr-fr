---
title: WM/ContainerFormat
description: L’attribut WM/ContainerFormat spécifie le type de fichier chargé dans l’objet appelant.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- Format Windows Media WM/ContainerFormat
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e0d5cc430b0580c6719d212d664d8c19ddc65eee64e5877a8e6aba80d94a6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839439"
---
# <a name="wmcontainerformat"></a>WM/ContainerFormat

L’attribut **WM/ContainerFormat** spécifie le type de fichier chargé dans l’objet appelant.

## <a name="global-constant"></a>Constante globale

\_wszWMContainerFormat g

## <a name="data-type"></a>Type de données

[**WMT \_ \_format de stockage**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (type de stockage **WMT \_ \_ binaire**)

## <a name="remarks"></a>Remarques

Cet attribut est utilisé à la place de **IWMProfile3 :: GetStorageFormat** et **IWMProfile3 :: SetStorageFormat**, qui ne sont plus pris en charge.

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




