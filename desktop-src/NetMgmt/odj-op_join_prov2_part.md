---
title: OP_JOINPROV2_PART
description: Définition du OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517757"
---
# <a name="op_joinprov2_part-structure"></a>Structure OP_JOINPROV2_PART

Contient des informations supplémentaires utilisées pour la configuration d’un client joint à un domaine.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Membres

### <a name="dwflags"></a>dwFlags

Doit être défini sur zéro ou sur l’une des valeurs suivantes :

|Valeur|Signification|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Le site spécifié dans lpSiteName doit être considéré comme le site permanent pour le client.|

### <a name="lpnetbiosname"></a>lpNetbiosName

Contient le nom NetBIOS du compte d’ordinateur au format Unicode.

### <a name="lpsitename"></a>lpSiteName

Contient le nom du site Active Directory que le client doit utiliser.

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

Contient le nom de domaine DNS principal que le client doit utiliser.

### <a name="dwreserved"></a>dwReserved

Réservé pour une utilisation ultérieure et doit avoir la valeur 0.

### <a name="lpreserved"></a>lpReserved

Réservé pour une utilisation ultérieure et doit avoir la valeur NULL.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
