---
description: Récupère les attributs de base pour l’objet fichier spécifié.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533738"
---
# <a name="ntqueryattributesfile-function"></a>NtQueryAttributesFile fonction)

\[Cette fonction peut être modifiée ou supprimée de Windows sans préavis.\]

Récupère les attributs de base pour l’objet fichier spécifié.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ObjectAttributes* \[ dans\]
</dt> <dd>

Pointeur vers une structure [d' \_ attributs d’objet](https://msdn.microsoft.com/library/aa491657.aspx) qui fournit les attributs à utiliser pour l’objet fichier.

</dd> <dt>

*FileInformation* \[ à\]
</dt> <dd>

Pointeur vers une structure [d' \_ \_ informations de base de fichier](https://msdn.microsoft.com/library/aa491634.aspx) pour recevoir les informations d’attribut de fichier retournées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un code NTSTATUS ou d’erreur.

Les formulaires et la signification des codes d’erreur de NTSTATUS sont répertoriés dans le fichier d’en-tête Ntstatus. h disponible dans le kit WDK et sont décrits dans la documentation WDK.

## <a name="remarks"></a>Notes

Cette fonction n’a aucun fichier d’en-tête associé. La bibliothèque d’importation associée, ntdll. lib, est disponible dans le kit WDK. Vous pouvez également utiliser les fonctions [**LoadLibrary**](-loadlibrary.md) et [**GetProcAddress**](-getprocaddress-.md) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 




