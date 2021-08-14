---
description: Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.
title: IStorageProviderCopyHook::CopyCallback
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook::CopyCallback
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 26fe9079e7fdf53809f8c0763fa38f271536f1339d16647936fb141f8d213be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677977"
---
# <a name="istorageprovidercopyhookcopycallback-method"></a>IStorageProviderCopyHook :: CopyCallback, méthode

Détermine si l’interpréteur de commandes est autorisé à déplacer, copier, supprimer ou renommer un dossier dans la racine de synchronisation d’un fournisseur de Cloud.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT CopyCallback( 
    HWND hwnd,
    UINT operation,
    UINT flags,
    LPCWSTR srcFile,
    DWORD srcAttribs,
    LPCWSTR destFile,
    DWORD destAttribs,
    UINT* result
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre que le gestionnaire de raccordement de copie doit utiliser comme parent pour tous les éléments d’interface utilisateur que le gestionnaire peut avoir besoin d’afficher. Si **FOF_SILENT** est spécifié dans l' *opération*, la méthode doit ignorer ce paramètre.

</dd> </dl>

<dl> <dt>

*opération* \[ dans\]
</dt> <dd>

Opération à exécuter. Ce paramètre peut être l’une des valeurs listées sous le membre **wFunc** de la structure [SHFILEOPSTRUCT](/windows/win32/api/shellapi/ns-shellapi-shfileopstructa) .

</dd> </dl>

<dl> <dt>

*indicateurs* \[ dans\]
</dt> <dd>

Indicateurs qui contrôlent l’opération. Ce paramètre peut être une ou plusieurs des valeurs listées sous le membre *fFlags* de la structure [SHFILEOPSTRUCT](/windows/desktop/api/shellapi/ns-shellapi-shfileopstructa) .

Pour les raccordements de copie d’imprimante, cette valeur est l’une des valeurs suivantes définies dans shellapi. h.

| Valeur       | Description |
|-------------|------------|
|  **PO_DELETE**      | Une imprimante est en cours de suppression. Le paramètre *srcFile* pointe vers le chemin d’accès complet à l’imprimante spécifiée.           |
|  **PO_RENAME**       | Une imprimante est renommée. Le paramètre *srcFile* pointe vers le nouveau nom de l’imprimante. Le paramètre *destFile* pointe vers l’ancien nom.           |
| **PO_PORTCHANGE**    | Non pris en charge. Ne pas utiliser.          |
| **PO_REN_PORT**    | Non pris en charge. Ne pas utiliser.           |

</dd> </dl>

<dl> <dt>

*srcFile* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du dossier source.

</dd> </dl>

*srcAttribs* \[ dans\]
</dt> <dd>

Attributs du dossier source. Ce paramètre peut être une combinaison de l’un des indicateurs d’attribut de fichier (FILE_ATTRIBUTE_ *) définis dans les fichiers d’en-tête. Consultez [constantes d’attribut de fichier](../fileio/file-attribute-constants.md).

</dd> </dl>

*destFile* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne qui contient le nom du dossier de destination.

</dd> </dl>

*destAttribs* \[ dans\]
</dt> <dd>

Attributs du dossier de destination. Ce paramètre peut être une combinaison de l’un des indicateurs d’attribut de fichier (FILE_ATTRIBUTE_ *) définis dans les fichiers d’en-tête. Consultez [constantes d’attribut de fichier](../fileio/file-attribute-constants.md).

</dd> </dl>

*résultat* \[ à\]
</dt> <dd>

Valeur entière qui indique si l’interpréteur de commandes doit effectuer l’opération. Celui-ci peut avoir l'une des valeurs suivantes :

| Value       | Description |
|-------------|------------|
| **IDYES**       | Autorise l’opération.           |
| **IDNO**        | Empêche l’opération sur ce dossier, mais continue avec les autres opérations qui ont été approuvées (par exemple, une opération de copie par lot).           |
| **IDCANCEL**    | Empêche l’opération en cours et annule toutes les opérations en attente.           |


</dd> </dl>


## <a name="return-value"></a>Valeur retournée

Retourne **S_OK** en cas de réussite, ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

L’interpréteur de commandes appelle le gestionnaire de raccordement de copie du fournisseur de Cloud pour chaque dossier sous la racine de synchronisation inscrite. pour inscrire un gestionnaire de raccordement de copie pour les dossiers cloud, définissez la valeur **CopyHook** sous la clé **HKEY_LOCAL_MACHINE/software/microsoft/Windows/CurrentVersion/Explorer/SyncRootManager/{SyncRootId}** sur le CLSID de l’objet de raccordement de copie.

Lorsque la méthode **CopyCallback** est appelée, l’interpréteur de commandes Initialise l’interface [IStorageProviderCopyHook](nn-shobjidl-istorageprovidercopyhook.md) directement sans utiliser d’abord une interface [IShellExtInit](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 10 Version préliminaire d’Insider 19624                                |
| En-tête                   | ShObjIdl. h   |

## <a name="see-also"></a>Voir aussi

[Créer un moteur de synchronisation Cloud qui prend en charge les fichiers d’espace réservé](../cfapi/build-a-cloud-file-sync-engine.md)