---
description: 'IStats :: Connecter méthode-la méthode Connecter connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.'
ms.assetid: 29a12df7-9c81-40ff-ac12-33ce1de833b1
title: 'IStats :: Connecter, méthode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6521e77453ec77f81422c7903b1a394512a4c1b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471185"
---
# <a name="istatsconnect-method"></a>IStats :: Connecter, méthode

la méthode **Connecter** connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hInputBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle le NPP se connecte et les informations de configuration pour cette connexion.

</dd> <dt>

*StatusCallbackProc* \[ dans\]
</dt> <dd>

Adresse de la fonction de rappel de l’utilisateur, qui reçoit les mises à jour d’État, telles que les déclencheurs. Si aucune fonction de rappel n’est utilisée, définissez ce paramètre et le paramètre *userContext* sur la **valeur null**.

</dd> <dt>

*UserContext* \[ dans\]
</dt> <dd>

Valeur passée lorsque la fonction de rappel de l’utilisateur est appelée. La valeur de ce paramètre est généralement HWND ou un pointeur’This'. Si aucune fonction de rappel n’est spécifiée, affectez la valeur **null** à ce paramètre et au paramètre *StatusCallbackProc* .

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IStats :: configure** ) :




| Code de retour | Description | 
|-------------|-------------|
| <dl><dt><strong>NMERR_ALREADY_CONNECTED</strong></dt></dl> | Cette instance de l’objet COM NPP est déjà connectée au réseau.<br /> | 
| <dl><dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt></dl> | L’objet BLOB de configuration est endommagé. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt></dl> | L’objet BLOB d’entrée spécifié par le paramètre <em>hInputBlob</em> n’a pas d’entrée nécessaire pour effectuer cette opération. cette erreur peut être générée par l’appel de <strong>IStats :: Connecter</strong> ou <strong>IStats :: configure</strong> . Examinez l’objet BLOB d’erreur retourné par <em>hErrorBlob</em> pour déterminer quelle entrée est introuvable.<br /> | 
| <dl><dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt></dl> | La fonction <strong>CreateBlob</strong> n’a pas été appelée. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt></dl> | La chaîne ne se termine pas par un caractère null. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt></dl> | La partie déclencheur de l’objet BLOB d’entrée est endommagée. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_INVALID_BLOB</strong></dt></dl> | L’objet spécifié dans <em>hInputBlob</em> n’est pas un objet BLOB. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt></dl> | Le répertoire de capture par défaut n’a pas été défini dans le registre. Pour définir le répertoire de capture, utilisez le chemin d’accès suivant. <br /><pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre> | 
| <dl><dt><strong>NMERR_OUT_OF_MEMORY</strong></dt></dl> | La mémoire requise pour effectuer cette opération n’était pas disponible. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_TIMEOUT</strong></dt></dl> | Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 
| <dl><dt><strong>NMERR_UPLEVEL_BLOB</strong></dt></dl> | Le numéro de version de l’objet BLOB spécifié dans <em>hInputBlob</em> est incorrect. Cette erreur est générée par l’appel de <strong>IStats :: configure</strong> .<br /> | 




 

## <a name="remarks"></a>Remarques

lorsque la méthode **Connecter** est appelée, Moniteur réseau appelle automatiquement la méthode **IStats :: configure** à l’aide de l’objet BLOB fourni par le paramètre *hInputBlob* . notez que les codes d’erreur retournés par l’appel à **IStats :: configure** sont passés en retour et retournés par l’appel de **IStats :: Connecter** .

Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames. Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser l’interface **IStats** pour capturer des frames.

L’objet BLOB d’entrée spécifié par *hInputBlob* peut être obtenu en appelant les méthodes **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable** .

L’objet BLOB d’erreur retourné par le paramètre *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*. L’objet BLOB d’erreurs renvoyé contient des informations d’erreur que l’application peut utiliser pour la résolution des problèmes. Par exemple, si l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée que Moniteur réseau n’a pas pu trouver est incluse dans l’objet blob d’erreur retourné.



| Pour obtenir des informations sur                                             | Consultez                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------|
| Obtention de l’objet BLOB d’entrée qui représente une carte d’interface réseau | [Sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[IStats :: configure](istats-configure.md)
</dt> <dt>

[IStats ::D éconnecter](istats-disconnect.md)
</dt> <dt>

[OBJETS BLOB Moniteur réseau](network-monitor-blobs.md)
</dt> </dl>

 

 




