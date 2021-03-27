---
UID: ''
title: SHGetFolderPathEx fonction)
description: Récupère le chemin d’accès d’un dossier connu identifié par KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2020
ms.locfileid: "104971659"
---
# <a name="shgetfolderpathex-function"></a>SHGetFolderPathEx fonction)

## <a name="description"></a>Description

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.
Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Récupère le chemin d’accès complet d’un dossier connu identifié par le [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)du dossier.
Cela étend [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) en vous permettant de définir la taille initiale de la mémoire tampon de la chaîne.

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a>Paramètres

### <a name="rfid-in"></a>RFID [in]

Référence au **KNOWNFOLDERID** qui identifie le dossier.

### <a name="dwflags-in"></a>dwFlags [in]

Indicateurs qui spécifient des options de récupération spéciales.
Cette valeur peut être 0 ; Sinon, une ou plusieurs des valeurs [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .

### <a name="htoken-in-optional"></a>hToken [in, facultatif]

[Jeton d’accès](/windows/desktop/SecAuthZ/access-tokens) qui représente un utilisateur particulier.
Si ce paramètre est **null**, ce qui correspond à l’utilisation la plus courante, la fonction demande le dossier connu pour l’utilisateur actuel.

Demandez le dossier d’un utilisateur spécifique en passant le *hToken* de cet utilisateur.
Cela s’effectue généralement dans le contexte d’un service qui dispose de privilèges suffisants pour récupérer le jeton d’un utilisateur donné.
Ce jeton doit être ouvert avec les droits [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) et [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .
Dans certains cas, vous devez également inclure des [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).
En plus de transmettre le *hToken* de l’utilisateur, la ruche de registre de cet utilisateur spécifique doit être montée.
Pour plus d’informations sur les problèmes de contrôle d’accès, consultez [Access Control](/windows/desktop/SecAuthZ/access-control) .

L’attribution du paramètre *hToken* la valeur-1 indique l’utilisateur par défaut.
Cela permet aux clients de [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) de trouver des emplacements de dossiers (tels que le dossier **Desktop** ) pour l’utilisateur par défaut.
Le profil utilisateur par défaut est dupliqué lorsqu’un nouveau compte d’utilisateur est créé, et il comprend des dossiers spéciaux tels que **documents** et **Bureau**.
Tous les éléments ajoutés au dossier utilisateur par défaut apparaissent également dans tout nouveau compte d’utilisateur.
Notez que l’accès aux dossiers utilisateur par défaut nécessite des privilèges d’administrateur.

### <a name="pszpath-out"></a>pszPath [out]

Chaîne Unicode terminée par le caractère null.
Cette mémoire tampon doit avoir une taille de cchPath.
Quand **SHGetFolderPathEx** retourne la valeur, ce paramètre contient le chemin d’accès au dossier connu.

### <a name="cchpath-in"></a>cchPath [in]

Taille de la mémoire tampon *ppszPath* , en caractères.

## <a name="returns"></a>Retours

Retourne **S_OK** en cas de réussite, ou une valeur d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Comme [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) est un wrapper pour [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), cette fonction (**SHGetFolderPathEx**) sert également d’extension à **SHGetFolderPath**.

## <a name="see-also"></a>Voir aussi

[KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)

[KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[SHGetKnownFolderIDList](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
