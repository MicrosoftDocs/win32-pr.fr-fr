---
description: Affiche une boîte de dialogue qui permet à un utilisateur de sélectionner un certificat.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: CryptUIDlgSelectCertificate, fonction
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: fb37eb664841331ce3f37e9ce37ca3ab9e5c0f92c254cff0896c6c682a9f2872
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768162"
---
# <a name="cryptuidlgselectcertificate-function"></a>CryptUIDlgSelectCertificate, fonction

La fonction **CryptUIDlgSelectCertificate** affiche une boîte de dialogue qui permet à un utilisateur de sélectionner un certificat.

## <a name="syntax"></a>Syntaxe


```C++
PCCERT_CONTEXT WINAPI CryptUIDlgSelectCertificate(
  _In_  PCCRYPTUI_SELECTCERTIFICATE_STRUCT pcsc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PCSC* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ struct SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) qui contient des informations sur la boîte de dialogue à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pointeur vers une structure [**de \_ contexte de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) qui représente le certificat sélectionné par l’utilisateur. Lorsque vous avez fini d’utiliser ce certificat, vous devez passer ce pointeur à la fonction [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) pour décrémenter le décompte de références du contexte de certificat.

Si le membre **dwFlags** de la structure *PCSC* ne contient pas l’indicateur de **\_ \_ multisélection CRYPTUI SELECTCERT** , une valeur de retour **null** signifie que l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificat.

Si le membre **dwFlags** de la structure *PCSC* contient l’indicateur **de \_ \_ multisélection CRYPTUI SELECTCERT** , cette fonction retourne toujours la **valeur null**. Les certificats sélectionnés seront contenus dans le magasin de certificats représenté par le membre **hSelectedCertStore** de *PCSC*. Si le nombre de certificats dans le magasin est identique avant et après l’appel de **CryptUIDlgSelectCertificate**, l’utilisateur a fermé la boîte de dialogue sans sélectionner de certificats.

## <a name="remarks"></a>Remarques

Si le membre **dwFlags** de la structure du [**\_ \_ struct cryptui SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) a la **valeur \_ CRYPTUI SELECTCERT \_ Legacy**, la boîte de dialogue héritée s’affiche. Dans le cas contraire, la boîte de dialogue de sélection de certificat active s’affiche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows XP uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                              |
| Fin de la prise en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                       |
| Bibliothèque<br/>                  | <dl> <dt>Cryptui. lib</dt> </dl>            |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>            |
| Noms Unicode et ANSI<br/>   | **CryptUIDlgSelectCertificateW** (Unicode) et **CryptUIDlgSelectCertificateA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SELECTCERTIFICATE, \_ struct**](cryptui-selectcertificate-struct.md)
</dt> </dl>






