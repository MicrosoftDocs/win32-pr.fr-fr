---
title: WM/StreamTypeInfo
description: L’attribut WM/StreamTypeInfo contient les informations de configuration du flux spécifié dans le fichier ASF.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- Format Windows Media WM/StreamTypeInfo
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380694"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

L’attribut **WM/StreamTypeInfo** contient les informations de configuration du flux spécifié dans le fichier ASF.

## <a name="global-constant"></a>Constante globale

\_wszWMStreamTypeInfo g

## <a name="data-type"></a>Type de données

[**WM \_ \_ \_ informations sur le type de flux**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ type WMT \_ binaire**)

## <a name="remarks"></a>Notes

Cet attribut s’applique à des flux spécifiques. Vous ne pouvez pas récupérer cet attribut pour le flux 0.

Cet attribut est en lecture seule.

L’objet de l’éditeur de métadonnées peut accéder à **WM/StreamTypeInfo** . Il s’agit de la seule façon d’accéder aux informations de configuration de flux sans ouvrir le fichier avec l’objet lecteur (ou l’objet lecteur synchrone).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




