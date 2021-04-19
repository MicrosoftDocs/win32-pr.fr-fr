---
description: Ouvre un objet d’annuaire existant.
ms.assetid: 7313fb32-976b-4c73-b9ba-09fb8ad7faf1
title: NtOpenDirectoryObject fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenDirectoryObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: ceea03c36e0617e2f48887275e7867e3589c87ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528659"
---
# <a name="ntopendirectoryobject-function"></a>NtOpenDirectoryObject fonction)

\[Cette fonction peut être modifiée ou non disponible à l’avenir.\]

Ouvre un objet d’annuaire existant.

## <a name="syntax"></a>Syntaxe


```C++
NTSTATUS WINAPI NtOpenDirectoryObject(
  _Out_ PHANDLE            DirectoryHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DirectoryHandle* \[ à\]
</dt> <dd>

Handle vers l’objet d’annuaire récemment ouvert.

</dd> <dt>

*DesiredAccess* \[ dans\]
</dt> <dd>

[**\_ Masque d’accès**](../secauthz/access-mask.md) qui spécifie l’accès demandé à l’objet d’annuaire. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                      | Signification                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="DIRECTORY_QUERY"></span><span id="directory_query"></span><dl> <dt>**Répertoire \_ REQUÊTE**</dt> <dt>0x0001</dt> </dl>                                            | Interroger l’accès à l’objet d’annuaire.<br/>                            |
| <span id="DIRECTORY_TRAVERSE"></span><span id="directory_traverse"></span><dl> <dt>**Répertoire \_ Parcourir**</dt> <dt>0x0002</dt> </dl>                                   | Nom : recherche l’accès à l’objet d’annuaire.<br/>                      |
| <span id="DIRECTORY_CREATE_OBJECT"></span><span id="directory_create_object"></span><dl> <dt>**Répertoire \_ CRÉER l' \_ objet**</dt> <dt>0x0004</dt> </dl>                   | Accès de création de nom à l’objet d’annuaire.<br/>                    |
| <span id="DIRECTORY_CREATE_SUBDIRECTORY"></span><span id="directory_create_subdirectory"></span><dl> <dt>**Répertoire \_ CRÉER un \_ sous-répertoire**</dt> <dt>0x0008</dt> </dl> | Sous-répertoire-création de l’accès à l’objet d’annuaire.<br/>            |
| <span id="DIRECTORY_ALL_ACCESS"></span><span id="directory_all_access"></span><dl> <dt>**Répertoire \_ Tous \_ les**</dt> droits d’accès <dt>standard \_ \_ requis \| 0xF</dt> </dl> | Tous les droits précédents et les **\_ droits standard \_ requis**.<br/> |



 

</dd> <dt>

*ObjectAttributes* \[ dans\]
</dt> <dd>

Attributs de l’objet d’annuaire. Pour initialiser la structure des **\_ attributs d’objet** , utilisez la macro **InitializeObjectAttributes** . Pour plus d’informations, consultez la documentation de ces éléments dans la documentation du kit WDK.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne l’état \_ Success ou un état d’erreur. Les codes d’État possibles sont les suivants :



| Code de retour                                                                                                       | Description                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ressources dont l’État est \_ insuffisant \_**</dt> </dl>    | Une mémoire tampon temporaire requise par cette fonction n’a pas pu être allouée.<br/>                                                                                                                                                                                                                           |
| <dl> <dt>**paramètre d’état \_ non valide \_**</dt> </dl>         | Le paramètre ObjectAttributes spécifié était un pointeur **null** , n’est pas un pointeur valide vers une structure d' **\_ attributs d’objet** , ou certains des membres spécifiés dans la structure des **\_ attributs** de l’objet n’étaient pas valides.<br/>                                                                          |
| <dl> <dt>**nom de l’objet d’état \_ \_ \_ non valide**</dt> </dl>      | Le paramètre *ObjectAttributes* contenait un membre **ObjectName** dans la structure d' **\_ attributs d’objet** qui n’était pas valide, car une chaîne vide a été trouvée après le caractère de **\_ \_ \_ séparation du chemin d’accès du nom d’objet** .<br/>                                                                        |
| <dl> <dt>**nom de l’objet d’état \_ \_ \_ \_ introuvable**</dt> </dl>   | Le paramètre *ObjectAttributes* contenait un membre **ObjectName** dans la structure des **\_ attributs** de l’objet qui est introuvable.<br/>                                                                                                                                                           |
| <dl> <dt>**\_ \_ chemin d’accès à l’objet d’état \_ \_ introuvable**</dt> </dl>   | Le paramètre *ObjectAttributes* contenait un membre **ObjectName** dans la structure d' **\_ attributs** de l’objet avec un chemin d’accès d’objet qui est introuvable. <br/>                                                                                                                                      |
| <dl> <dt>**État \_ \_syntaxe du chemin d’accès à l’objet \_ \_ incorrecte**</dt> </dl> | Le paramètre *ObjectAttributes* ne contenait pas de membre **RootDirectory** , mais le membre **ObjectName** dans la structure des **\_ attributs** de l’objet était une chaîne vide ou ne contient pas de caractère de **\_ \_ \_ séparation du chemin d’accès au nom** de l’objet. Cela indique une syntaxe incorrecte pour le chemin d’accès de l’objet.<br/> |



 

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NtQueryDirectoryObject**](ntquerydirectoryobject.md)
</dt> </dl>

 

 
