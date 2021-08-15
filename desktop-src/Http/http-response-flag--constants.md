---
title: Constantes HTTP_RESPONSE_FLAG_ (http. h)
description: Définissez les options de configuration des réponses dans l’API du serveur HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3099012df5be9ed4a53d3072319be6dc47ede32b71567749c4668cd7870fee29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118394407"
---
# <a name="http_response_flag_-constants"></a>\_ \_ Constantes d’indicateur de réponse http \_

Les constantes de l' **\_ \_ \_ indicateur de réponse http** définissent les options permettant de configurer les réponses dans l’API du serveur http.

Ces constantes sont utilisées dans le membre **Flags** de la structure de [**\_ réponse http \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .

<dl> <dt>

<span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**indicateur de réponse HTTP- \_ \_ \_ plusieurs \_ encodages \_ disponibles**
</dt> <dd> <dl> <dt>



Les encodages autres que le format d’identité sont disponibles pour cette ressource. Cet indicateur est ignoré si l’application n’a pas demandé la mise en cache de la réponse. Il est utilisé comme indicateur de l’API du serveur HTTP pour la négociation de contenu lors de la fourniture à partir du cache de réponse du noyau.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Http. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de la version 2,0 de l’API du serveur HTTP](http-server-api-version-2-0-constants.md)
</dt> <dt>

[**\_Réponse http \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





