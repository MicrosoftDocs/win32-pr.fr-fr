---
description: La méthode Connect connecte le NPP au réseau à l’aide d’une carte d’interface réseau spécifiée et fournit des informations de configuration sur la connexion.
ms.assetid: aae9ff9c-d077-4db2-a900-9916e4f7bb8b
title: 'IDelaydC :: Connect, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b2cd1fb5ad694493c4a225aa3bf109d7775b9dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861998"
---
# <a name="idelaydcconnect-method"></a>IDelaydC :: Connect, méthode

La méthode **Connect** connecte le NPP au réseau à l’aide d’une carte d’interface réseau spécifiée et fournit des informations de configuration sur la connexion.

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

Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle vous vous connectez et les informations de configuration relatives à cette connexion.

</dd> <dt>

*StatusCallbackProc* \[ dans\]
</dt> <dd>

Adresse de la fonction de rappel de l’utilisateur, qui est utilisée pour recevoir des mises à jour d’État, telles que les déclencheurs. Si aucune fonction de rappel n’est utilisée, définissez ce paramètre et le paramètre *userContext* sur la **valeur null**.

</dd> <dt>

*UserContext* \[ dans\]
</dt> <dd>

Valeur passée lorsque la fonction de rappel de l’utilisateur est appelée. La valeur de ce paramètre est généralement HWND ou un pointeur’This'. Si aucune fonction de rappel n’est spécifiée, affectez la valeur **null** à ce paramètre et au paramètre *StatusCallbackProc* .

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IDelaydC :: configure** ) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Code de retour</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>NMERR_ALREADY_CONNECTED</strong></dt> </dl></td>
<td>Cette instance de l’objet COM NPP est déjà connectée au réseau.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_CONVERSION_ERROR</strong></dt> </dl></td>
<td>L’objet BLOB de configuration est endommagé. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_ENTRY_DOES_NOT_EXIST</strong></dt> </dl></td>
<td>Une entrée nécessaire à l’exécution de cette opération est manquante dans l’objet BLOB d’entrée spécifié par <em>hInputBlob</em> . Cette erreur peut être générée par l’appel de <strong>IDelaydC :: Connect</strong> ou <strong>IDelaydC :: configure</strong> . Examinez l’objet BLOB d’erreur retourné par <em>hErrorBlob</em> pour déterminer quelle entrée est introuvable.<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_BLOB_NOT_INITIALIZED</strong></dt> </dl></td>
<td>La fonction <strong>CreateBlob</strong> n’a pas été appelée. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_BLOB_STRING_INVALID</strong></dt> </dl></td>
<td>La chaîne ne se termine pas par un caractère null. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_ILLEGAL_TRIGGER</strong></dt> </dl></td>
<td>La partie déclencheur de l’objet BLOB d’entrée est endommagée. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_INVALID_BLOB</strong></dt> </dl></td>
<td>L’objet spécifié dans <em>hInputBlob</em> n’est pas un objet BLOB. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_NO_DEFAULT_CAPTURE_DIRECTORY</strong></dt> </dl></td>
<td>Le répertoire de capture par défaut n’a pas été défini dans le registre. Utilisez le chemin d’accès suivant pour définir le répertoire de capture. <br/>
<pre class="syntax" data-space="preserve"><code>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\nm\Parameters\CapturePath</code></pre></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_OUT_OF_MEMORY</strong></dt> </dl></td>
<td>Aucune mémoire n’était disponible pour effectuer cette opération. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="even">
<td><dl> <dt><strong>NMERR_TIMEOUT</strong></dt> </dl></td>
<td>Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
<tr class="odd">
<td><dl> <dt><strong>NMERR_UPLEVEL_BLOB</strong></dt> </dl></td>
<td>Le numéro de version de l’objet BLOB spécifié dans <em>hInputBlob</em> est incorrect. Cette erreur est générée par l’appel de <strong>IDelaydC :: configure</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Lorsque la méthode **Connect** est appelée, le NPP appelle automatiquement **IDelaydC :: configure** à l’aide de l’objet BLOB fourni par *hInputBlob*. Notez que les codes d’erreur retournés par l’appel à **IDelaydC :: configure** sont passés en retour et retournés par l’appel de **IDelaydC :: Connect** .

Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames. Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser les méthodes de l’interface **IDelaydC** pour capturer des frames.

L’objet BLOB d’entrée spécifié par le paramètre *hInputBlob* peut être obtenu en appelant **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable**.

L’objet BLOB d’erreur retourné dans *hErrorBlob* contient des informations d’erreur que le développeur ou l’application peut utiliser pour la résolution des problèmes. L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.



| Pour obtenir des informations sur                          | Consultez                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtention de l’objet BLOB d’entrée qui représente une carte réseau | [Sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC :: configure](idelaydc-configure.md)
</dt> <dt>

[IDelaydC ::D éconnecter](idelaydc-disconnect.md)
</dt> <dt>

[IDelaydC :: Start](idelaydc-start.md)
</dt> </dl>

 

 




