---
title: Élément FastReconnect (EapType)
description: En savoir plus sur l’élément FastReconnect (EapType). Cet élément indique s’il faut effectuer une reconnexion rapide.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Élément FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bda956d698ebefef956e85557c6d940baa02f6bcc9ef7cca0081fd668107e18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119238719"
---
# <a name="fastreconnect-eaptype-element"></a>Élément FastReconnect (EapType)

L’élément **FastReconnect (EapType)** indique s’il faut effectuer une reconnexion rapide.

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

L’élément **FastReconnect** est défini par l’élément [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .

## <a name="remarks"></a>Remarques

Si l’élément **FastReconnect** a la valeur true, PEAP tente d’effectuer une reconnexion rapide ; Si la valeur est FALSe, PEAP effectue l’authentification complète. L’élément **FastReconnect** est facultatif.

## <a name="requirements"></a>Configuration requise



| Fonction | Version minimale du système d’exploitation prise en charge |
|------|------------------------------|
| Client<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Contexte de définition de l’élément dans le schéma**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

**Élément parent immédiat possible dans l’instance de schéma**
</dt> <dt>

[**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost et schéma hérité](eaphost-schemas.md)
</dt> <dt>

[Schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[Éléments de schéma mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





