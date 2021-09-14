---
title: Méthode Revoke de la classe Win32_TSIssuedLicense
description: Révoque les licences d’accès client par périphérique Services Bureau à distance (RDS \ 160 ; Licences d’accès client par périphérique) qui sont représentées par l' \_ objet Win32 TSIssuedLicense. Il ne s’agit pas d’une fonction statique.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Revoke, méthode Services Bureau à distance
- Revoke, méthode Services Bureau à distance, classe Win32_TSIssuedLicense
- Win32_TSIssuedLicense de la classe Services Bureau à distance, Revoke, méthode
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324518"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Méthode Revoke de la \_ classe TSIssuedLicense Win32

Révoque les licences d’accès client Services Bureau à distance par périphérique (CAL par périphérique) qui sont représentées par l’objet [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) . Il ne s’agit pas d’une fonction statique.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RevokableCals* \[ à\]
</dt> <dd>

Nombre de licences d’accès client aux services Bureau à distance du même type que l’objet actuel qui peut être révoqué.

</dd> <dt>

*NextRevokeAllowedOn* \[ à\]
</dt> <dd>

Date à laquelle l’administrateur peut ensuite tenter de révoquer des licences. Ce paramètre contient uniquement des données valides lorsque l’appel de la méthode **Revoke** a échoué, car le nombre maximal de révocations a été atteint.

</dd> </dl>

## <a name="remarks"></a>Notes

Vous devez être membre du groupe administrateurs pour appeler cette méthode.

Seules les CAL par périphérique peuvent être révoquées.

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Espace de noms<br/>                | Racine\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> </dl>

 

