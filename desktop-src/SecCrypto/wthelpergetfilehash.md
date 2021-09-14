---
description: Vérifie la signature d’un fichier signé et obtient la valeur de hachage et l’identificateur d’algorithme pour le fichier.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416350"
---
# <a name="wthelpergetfilehash-function"></a>WTHelperGetFileHash fonction)

\[La fonction **WTHelperGetFileHash** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]

La fonction **WTHelperGetFileHash** vérifie la signature d’un fichier signé et obtient la valeur de hachage et l’identificateur d’algorithme pour le fichier.

> [!Note]  
> Cette fonction n’est pas déclarée dans un fichier d’en-tête publié. Pour utiliser cette fonction, déclarez-la dans le format exact indiqué. Cette fonction n’a pas non plus de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Wintrust.dll.

 

## <a name="syntax"></a>Syntaxe


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pwszFilename* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui contient le chemin d’accès et le nom de fichier du fichier pour lequel obtenir le hachage.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*pvReserved* \[ in, out, facultatif\]
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la **valeur null**.

</dd> <dt>

*pbFileHash* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon destinée à recevoir la valeur de hachage du fichier. Le paramètre *pcbFileHash* contient la taille de cette mémoire tampon.

</dd> <dt>

*pcbFileHash* \[ in, out, facultatif\]
</dt> <dd>

Pointeur vers une variable **DWORD** qui, en entrée, contient la taille, en octets, de la mémoire tampon *pbFileHash* et, à la sortie, reçoit la taille, en octets, de la valeur de hachage.

Pour obtenir la taille requise de la valeur de hachage, transmettez la valeur **null** pour le paramètre *pbFileHash* . Cette fonction place la taille requise, en octets, de la valeur de hachage à cet emplacement.

Si le paramètre *pbFileHash* n’est pas **null** et que la taille n’est pas assez grande pour recevoir la valeur de hachage, cette fonction placera la taille requise, en octets, à cet emplacement et retournera l' **erreur plus de \_ \_ données**.

</dd> <dt>

*pHashAlgid* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une variable [**d' \_ ID ALG**](alg-id.md) pour recevoir l’identificateur de l’algorithme utilisé pour créer la valeur de hachage. Ce paramètre peut avoir la **valeur null** si cette information n’est pas nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un code d’État qui indique la réussite ou l’échec de la fonction.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code de retour                                                                                               | Description                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR de \_ réussite**</dt> </dl>             | Le fichier est signé et la signature a été vérifiée.<br/>                                                                                        |
| <dl> <dt>**ERREUR \_ plus de \_ données**</dt> </dl>          | Le paramètre *pbFileHash* n’est pas **null**, et la taille spécifiée par le paramètre *pcbFileHash* n’est pas assez grande pour recevoir le hachage.<br/> |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl> | Un échec d’allocation de mémoire s’est produit.<br/>                                                                                                      |
| <dl> <dt>**CONFIANCE \_ E \_ condensé incorrect \_**</dt> </dl>      | La signature du fichier n’a pas été vérifiée.<br/>                                                                                                |
| <dl> <dt>**APPROUVER \_ E \_ NoSignature**</dt> </dl>      | Le fichier n’a pas été signé ou a une signature qui n’est pas valide.<br/>                                                                              |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
