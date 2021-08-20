---
description: 'Fonction SetAsyncTraceParamsEx : termine la configuration d’une mémoire tampon de suivi avec des champs facultatifs pour les traces de style sprintf.'
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
ms.openlocfilehash: 6c41369e8a0d73a56dc5d9d831d0028e87a7ecec300f2e43a625f17bd25bede1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538863"
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

## <a name="remarks"></a>Remarques

Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
