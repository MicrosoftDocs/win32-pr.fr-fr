---
description: Définit la sécurité d’une clé de Registre ouverte dans une ruche de Registre hors connexion.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: ORSetKeySecurity, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545339"
---
# <a name="orsetkeysecurity-function"></a>ORSetKeySecurity fonction)

Définit la sécurité d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
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

Indicateurs binaires qui indiquent le type d’informations de sécurité à définir. Ce paramètre peut être une combinaison des indicateurs binaires d' [ \_ informations de sécurité](../secauthz/security-information.md) .

</dd> <dt>

*pSecurityDescriptor* \[ dans\]
</dt> <dd>

Pointeur vers une structure [de \_ descripteur de sécurité](/windows/win32/api/winnt/ns-winnt-security_descriptor) qui spécifie les attributs de sécurité à définir pour la clé spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne une erreur de \_ réussite.

Si la fonction échoue, elle retourne un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Bibliothèque du Registre hors connexion Windows version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORGetKeySecurity**](orgetkeysecurity.md)
</dt> <dt>

[descripteur de sécurité \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[informations de sécurité \_](../secauthz/security-information.md)
</dt> </dl>

 

 
