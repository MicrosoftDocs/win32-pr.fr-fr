---
description: Récupère une copie du descripteur de sécurité protégeant la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: ORGetKeySecurity, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 786321db22c513e7698fcd1661d173ccb5fdf76f1b09d9dd3e739ddf3fb2ca47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984159"
---
# <a name="orgetkeysecurity-function"></a>ORGetKeySecurity fonction)

Récupère une copie du descripteur de sécurité protégeant la clé de Registre ouverte spécifiée dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*SecurityInformation* \[ dans\]
</dt> <dd>

Valeur [des \_ informations de sécurité](../secauthz/security-information.md) qui indique les informations de sécurité demandées.

</dd> <dt>

*pSecurityDescriptor* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une copie du descripteur de sécurité demandé. Ce paramètre peut être **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in, out\]
</dt> <dd>

Pointeur vers une variable qui spécifie la taille, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pSecurityDescriptor* . Lorsque la fonction retourne, la variable contient le nombre d’octets écrits dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne une erreur de \_ réussite.

Si la fonction échoue, elle retourne un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si la mémoire tampon spécifiée par le paramètre *pSecurityDescriptor* est trop petite, la fonction retourne l’erreur \_ mémoire tampon insuffisante \_ et le paramètre *lpcbSecurityDescriptor* contient le nombre d’octets requis pour le descripteur de sécurité demandé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[informations de sécurité \_](../secauthz/security-information.md)
</dt> </dl>

 

 
