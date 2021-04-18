---
description: Ferme un handle vers un fournisseur de tickets d’impression.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520553"
---
# <a name="unbindptproviderthunk-function"></a>UnbindPTProviderThunk fonction)

\[Cette fonction n’est pas prise en charge et peut être désactivée ou supprimée dans les versions futures de Windows. [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fournit des fonctionnalités équivalentes et doit être utilisé à la place.\]

Ferme un handle vers un fournisseur de tickets d’impression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hProvider* \[ dans\]
</dt> <dd>

Handle d’un fournisseur de tickets d’impression ouvert. Ce descripteur est retourné par la fonction [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur **HRESULT** . Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Schéma d’impression](./printschema.md)
</dt> <dt>

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

