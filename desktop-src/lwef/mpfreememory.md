---
title: MpFreeMemory, fonction (MpClient. h)
description: Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741012"
---
# <a name="mpfreememory-function"></a>MpFreeMemory fonction)

Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants. Toutes les mémoires tampons allouées et renvoyées par les fonctions de protection contre les programmes malveillants doivent être libérées par l’appelant à l’aide de cette fonction.

## <a name="syntax"></a>Syntaxe


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pMemory* \[ dans\]
</dt> <dd>

Type : **pVoid**

Pointeur vers la mémoire allouée par une fonction de protection contre les programmes malveillants.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour faciliter la gestion de la mémoire pour les clients, le gestionnaire de protection contre les programmes malveillants définit également des macros pour libérer la mémoire associée aux différentes structures renvoyées par les fonctions de protection contre les programmes malveillants Les macros suivantes sont définies dans le fichier d’en-tête mpmemfree. h :



| Nom                            | Description                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| MPRESOURCE \_ informations \_ gratuites          | Libère des [**\_ informations MPRESOURCE**](mpresource-info.md)allouées.                  |
| MPTHREAT \_ informations \_ gratuites            | Libère des [**\_ informations MPTHREAT**](mpthreat-info.md)allouées.                      |
| MPTHREAT \_ \_ informations localisées \_ gratuites | Libère des [**\_ \_ informations localisées MPTHREAT**](mpthreat-localized-info.md)allouées. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**\_informations MPRESOURCE**](mpresource-info.md)
</dt> <dt>

[**\_informations MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**\_informations localisées \_ MPTHREAT**](mpthreat-localized-info.md)
</dt> </dl>

 

 





