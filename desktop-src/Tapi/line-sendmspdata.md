---
description: Le message SENDMSPDATA de la ligne TSPI \_ est envoyé lorsque le fournisseur de services de téléphonie (TSP) souhaite transmettre des informations au fournisseur de services multimédia (MSP).
ms.assetid: 982f40b3-7758-493c-9d04-6480e3c9e86d
title: Message LINE_SENDMSPDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce46664be0bc7f312af8b45cc5e06e13a7d91488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525200"
---
# <a name="line_sendmspdata-message"></a>\_Message SENDMSPDATA de ligne

Le message **\_ SENDMSPDATA** de la ligne TSPI est envoyé lorsque le fournisseur de services de téléphonie (TSP) souhaite transmettre des informations au fournisseur de services multimédia (MSP).


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htLine* 
</dt> <dd>

Handle TAPI pour la ligne.

</dd> <dt>

*htCall* 
</dt> <dd>

Handle TAPI pour l’appel.

</dd> <dt>

*dwMsg* 
</dt> <dd>

La ligne de valeur \_ SENDMSPDATA.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identifie le MSP qui doit recevoir le message. Si la valeur est 0, le message est envoyé à tous les MSP. Il s’agit du handle qui est passé à la fonction [**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance) .

</dd> <dt>

*dwParam2* 
</dt> <dd>

Mémoire tampon à transmettre au MSP. La mémoire tampon n’est pas interprétée par TAPI.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Taille, en octets, de la mémoire tampon dans *dwParam2*.

</dd> </dl>

## <a name="remarks"></a>Notes

Le fournisseur de services doit négocier une version TAPI 3,0 ou ultérieure pour que ce message fonctionne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,2<br/>                                                      |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[À propos du fournisseur de services multimédia (MSP)](./about-the-media-service-provider-msp-.md)
</dt> <dt>

[**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
</dt> <dt>

[**TSPI \_ LineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
</dt> <dt>

[**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
</dt> <dt>

[**TSPI \_ lineRecieveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
</dt> <dt>

[**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)
</dt> </dl>

 

