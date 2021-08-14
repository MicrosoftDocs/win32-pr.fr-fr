---
description: La \_ propriété NewEnum des certificats récupère une interface IEnumVARIANT sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eab4395e24b12b8e9492c6f18f595a91e192a59c53309411433b49881cd4fd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770511"
---
# <a name="certificates_newenum-property"></a>Certificats. \_ NewEnum, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **\_ NewEnum** récupère une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection. cette propriété est masquée dans Visual Basic scripting Edition (VBScript).

## <a name="syntax"></a>Syntaxe


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a>Valeur de la propriété

Une interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) sur un objet qui peut être utilisé pour énumérer la collection.

## <a name="remarks"></a>Remarques

cette propriété est automatiquement utilisée en interne lorsque vous utilisez la `For Each In` construction dans Visual Basic scripting Edition (VBScript).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Certificates**](certificates.md)
</dt> </dl>

 

 
