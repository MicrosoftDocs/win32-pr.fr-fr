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
ms.openlocfilehash: 6fb40926d5ecba3aea2c7f2db64850152c66a25861d4422fddf04670c76d8148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698271"
---
# <a name="wmstreamtypeinfo"></a>WM/StreamTypeInfo

L’attribut **WM/StreamTypeInfo** contient les informations de configuration du flux spécifié dans le fichier ASF.

## <a name="global-constant"></a>Constante globale

\_wszWMStreamTypeInfo g

## <a name="data-type"></a>Type de données

[**WM \_ \_ \_ informations sur le type de flux**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**\_ type WMT \_ binaire**)

## <a name="remarks"></a>Remarques

Cet attribut s’applique à des flux spécifiques. Vous ne pouvez pas récupérer cet attribut pour le flux 0.

Cet attribut est en lecture seule.

L’objet de l’éditeur de métadonnées peut accéder à **WM/StreamTypeInfo** . Il s’agit de la seule façon d’accéder aux informations de configuration de flux sans ouvrir le fichier avec l’objet lecteur (ou l’objet lecteur synchrone).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




