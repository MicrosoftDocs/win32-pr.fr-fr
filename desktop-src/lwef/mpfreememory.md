---
title: MpFreeMemory, fonction (MpClient. h)
description: Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- fonctionnalités d’environnement Windows hérités de la fonction MpFreeMemory
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
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247424"
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
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                    |
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

 

 





