---
description: Exporte le matériel de génération de clé selon la norme RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: SslExportKeyingMaterial, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013618"
---
# <a name="sslexportkeyingmaterial-function"></a>SslExportKeyingMaterial fonction)

Exporte le matériel de génération de clé selon la [norme RFC 5705](https://tools.ietf.org/html/rfc5705). Cette fonction utilise la fonction TLS aléatoire pour produire une mémoire tampon d’octets de l’élément de clé. Elle prend une référence au secret principal, l’étiquette disambiguating ASCII, les valeurs aléatoires client et serveur, et éventuellement les données de contexte de l’application.

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSslProvider* \[ dans\]
</dt> <dd>

Handle de l’instance du fournisseur de protocole TLS.

</dd> <dt>

*hMasterKey* \[ dans\]
</dt> <dd>

Handle de l’objet de clé principale qui sera utilisé pour créer le support de génération de clés à br exporté.

</dd> <dt>

*slabel* \[ dans\]
</dt> <dd>

chaîne d’étiquette ASCII terminée par un caractère NUL. Schannel supprime le caractère null de fin avant de le passer à la fonction Pseudo-aléatoire.

</dd> <dt>

*pbRandoms* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient une concaténation des valeurs aléatoires *\_ aléatoires du client* et du *serveur \_* de la connexion TLS.

</dd> <dt>

*cbRandoms* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbRandoms* .

</dd> <dt>

*pbContextValue* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le contexte d’application. Si *pbContextValue* a la **valeur null**, *cbContextValue* doit être égal à zéro.

</dd> <dt>

*cbContextValue* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbContextValue* .

</dd> <dt>

*pbOutput* \[ à\]
</dt> <dd>

Adresse d’une mémoire tampon qui reçoit le support de génération de clé exporté. Le paramètre *cbOutput* contient la taille de cette mémoire tampon. Cette valeur ne peut pas être **null**.

</dd> <dt>

*cbOutput* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon *pbOutput* . Doit être supérieur à zéro.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Non utilisé. Doit être défini à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, elle retourne zéro.

Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.

Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.



| Code/valeur de retour                                                                                                                                                    | Description                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt> </dl> | L’un des handles fournis n’est pas valide.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




