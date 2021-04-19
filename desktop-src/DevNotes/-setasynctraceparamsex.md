---
description: Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style sprintf.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538097"
---
# <a name="setasynctraceparamsex-function"></a>SetAsyncTraceParamsEx fonction)

Termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style **sprintf**.

## <a name="syntax"></a>Syntaxe


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszModule* 
</dt> <dd>

Nom du module associé à la trace.

</dd> <dt>

*pszFile* 
</dt> <dd>

Nom du fichier source qui contient l’exception.

</dd> <dt>

*Tâche* 
</dt> <dd>

Numéro de ligne de l’exception dans le fichier source.

</dd> <dt>

*pszFunction* 
</dt> <dd>

Nom de fonction de l’exception.

</dd> <dt>

*dwTraceMask* 
</dt> <dd>

Constante d’indicateur de trace qui représente l’un des types de suivi disponibles. Ce paramètre peut prendre l’une des valeurs suivantes.

<dl> <dt>

<span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**Erreur irrécupérable \_ \_Masque de trace** (0x00000001)
</dt> <dt>

<span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Erreur \_ \_Masque de trace** (0x00000002)
</dt> <dt>

<span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Débogage \_ \_Masque de trace** (0x00000004)
</dt> <dt>

<span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**État \_ \_Masque de trace** (0x00000008)
</dt> <dt>

<span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**\_ FUNCT \_Masque de trace** (0x00000010)
</dt> <dt>

<span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Message \_ \_Masque de trace** (0x00000020)
</dt> <dt>

<span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Tout \_ \_Masque de trace** (0xFFFFFFFF)
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne 1 si la fonction est réussie ; Sinon, elle retourne 0.

## <a name="remarks"></a>Notes

Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
