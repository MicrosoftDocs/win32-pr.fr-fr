---
description: Le message CREATEDIALOGINSTANCE de la ligne TSPI fait en sorte que l' \_ interface TAPI crée une association entre le fournisseur de services et une instance de la \_ fonction TUISPI providerGenericDialog s’exécutant dans le contexte de l’application.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Message LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532866"
---
# <a name="line_createdialoginstance-message"></a>\_Message CREATEDIALOGINSTANCE de ligne

Le message **\_ CREATEDIALOGINSTANCE** de la ligne TSPI fait que l’interface TAPI crée une association entre le fournisseur de services et une instance de la fonction [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) s’exécutant dans le contexte de l’application qui a appelé la fonction TSPI asynchrone identifiée par le paramètre *DwRequestID* de la structure [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) désignée par *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* 
</dt> <dd>

ProviderHandle fourni au fournisseur de services en tant que paramètre pour [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Pointeur vers une structure [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

