---
description: Crée la clé de Registre spécifiée dans une ruche de Registre hors connexion. Si la clé existe déjà, la fonction l’ouvre.
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: ORCreateKey, fonction (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: b7ea5a365a9c5bdcb478ce47443a713ed5bc091666b54de880dc478708e4c36c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749689"
---
# <a name="orcreatekey-function"></a>ORCreateKey fonction)

Crée la clé de Registre spécifiée dans une ruche de Registre hors connexion. Si la clé existe déjà, la fonction l’ouvre.

## <a name="syntax"></a>Syntaxe


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Gérer* \[ dans\]
</dt> <dd>

Handle d’une clé de Registre ouverte dans une ruche de Registre hors connexion.

</dd> <dt>

*lpSubKey* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le nom d’une sous-clé que cette fonction ouvre ou crée. Le paramètre *lpSubKey* doit spécifier une sous-clé de la clé identifiée par le paramètre *handle* ; Il peut atteindre jusqu’à 32 niveaux de profondeur dans l’arborescence du Registre. Pour plus d’informations sur les noms de clé, consultez [structure du Registre](../sysinfo/structure-of-the-registry.md).

Ce paramètre ne peut pas être **null**.

Les noms de clés ne respectent pas la casse.

</dd> <dt>

*lpClass* \[ dans, facultatif\]
</dt> <dd>

Classe (type d’objet) de cette clé. Ce paramètre peut être ignoré. Ce paramètre peut être **NULL**.

</dd> <dt>

*dwOptions* \[ dans, facultatif\]
</dt> <dd>

Ce paramètre peut avoir la valeur 0 ou l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                          | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <dt>**Reg \_ OPTION de \_ création de \_ lien**</dt> <dt>0x00000002L</dt> </dl>    | La clé est un lien symbolique. Le chemin d’accès cible est assigné à la valeur de L' « SymbolicLinkValue » de la clé. Le chemin d’accès cible doit être un chemin d’accès absolu au registre. Si cette option est définie, **l' \_ option reg \_ non \_ volatile** doit également être définie. <br/> Si le paramètre *lpSubKey* spécifie une clé existante, il doit avoir été créé avec l' **\_ option reg \_ Create \_ Link**.<br/> Les liens symboliques du Registre doivent être utilisés uniquement lorsque cela est absolument nécessaire pour la compatibilité des applications. <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <dt>**Reg \_ OPTION \_ non \_ volatile**</dt> <dt>0x00000000L</dt> </dl> | La clé n’est pas volatile. Il s’agit de la valeur par défaut. Les informations sont stockées dans un fichier et sont conservées lorsque le système est redémarré. La fonction [**ORSaveHive**](orsavehive.md) enregistre les clés qui ne sont pas volatiles.<br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pSecurityDescriptor* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure [de \_ descripteur de sécurité](/windows/win32/api/winnt/ns-winnt-security_descriptor) qui contient un descripteur de sécurité pour la nouvelle clé. Si *pSecurityDescriptor* a la **valeur null**, la clé obtient un descripteur de sécurité par défaut. Les listes de contrôle d’accès dans un descripteur de sécurité par défaut pour une clé sont héritées de sa clé parente directe.

</dd> <dt>

*phkResult* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit un handle vers la clé ouverte ou créée. Utilisez la fonction [**ORCloseKey**](orclosekey.md) pour fermer la clé une fois que vous avez fini d’utiliser le handle.

</dd> <dt>

*pdwDisposition* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable qui reçoit l’une des valeurs de disposition suivantes.



| Valeur                                                                                                                                                                                                                                                          | Signification                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <dt>**Reg \_ \_Nouvelle \_ clé**</dt> <dt>0x00000001L</dt> créée </dl>             | La clé n’existait pas et a été créée.<br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <dt>**Reg \_ 0x00000002L \_ \_ clé existante ouverte**</dt> <dt></dt> </dl> | La clé existait et a simplement été ouverte sans être modifiée.<br/> |



 

Si *pdwDisposition* a la **valeur null**, aucune information de disposition n’est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur différent de zéro défini dans Winerror. h. Vous pouvez utiliser la fonction [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) avec le format \_ message \_ de l' \_ indicateur système pour obtenir une description générique de l’erreur.

Si le paramètre *dwOptions* est défini avec **l' \_ option reg \_ Create \_ Link** mais que l' **\_ option reg \_ non \_ volatile** est désactivée, ou si le handle à retourner est un descripteur de la clé racine de Hive, la fonction retourne un paramètre d’erreur \_ non valide \_ .

## <a name="remarks"></a>Remarques

La clé créée par la fonction **ORCreateKey** n’a pas de valeur. Une application peut utiliser la fonction [**ORSetValue**](orsetvalue.md) pour définir des valeurs de clés.

La fonction **ORCreateKey** ne peut pas être utilisée pour créer la clé racine dans une ruche de Registre hors connexion. Utilisez la fonction [**ORCreateHive**](orcreatehive.md) pour créer la clé racine et obtenir un descripteur de la clé.

Le registre hors connexion ne prend pas en charge l’enregistrement de clés individuelles. Utilisez la fonction [**ORSaveHive**](orsavehive.md) pour enregistrer une clé et ses sous-clés dans une ruche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|---------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | Windows Bibliothèque de Registre hors connexion version 1,0 ou ultérieure<br/>                      |
| En-tête<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateHive**](orcreatehive.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[descripteur de sécurité \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
