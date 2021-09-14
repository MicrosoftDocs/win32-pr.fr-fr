---
description: 'IRTC :: Connecter méthode-la méthode Connecter connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.'
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'IRTC :: Connecter, méthode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ba62f3341b18ddfdbf09af4eec701322d901ab79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127119234"
---
# <a name="irtcconnect-method"></a>IRTC :: Connecter, méthode

la méthode **Connecter** connecte le NPP au réseau à l’aide d’une carte réseau spécifiée et fournit des informations de configuration pour la connexion.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hInputBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB qui spécifie la carte réseau à laquelle vous vous connectez et les informations de configuration pour cette connexion.

</dd> <dt>

*StatusCallbackProc* \[ dans\]
</dt> <dd>

Adresse de la fonction de rappel d’état de l’utilisateur, qui reçoit les mises à jour d’État, telles que les déclencheurs. Ce paramètre peut avoir la valeur **null**.

</dd> <dt>

*FramesCallbackProc* \[ dans\]
</dt> <dd>

Adresse de la fonction de rappel de frame de l’utilisateur, qui est utilisée pour recevoir des mises à jour d’État, telles que les déclencheurs. Ce paramètre peut avoir la valeur **null**.

</dd> <dt>

*UserContext* \[ dans\]
</dt> <dd>

Valeur passée lorsque l’état de l’utilisateur et la fonction de rappel de frame sont appelés. Si les deux fonctions de rappel sont spécifiées, elles doivent utiliser la même valeur de contexte utilisateur. La valeur de ce paramètre est généralement HWND ou un pointeur’This'.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreur qui contient des informations supplémentaires sur l’erreur. Pour plus d’informations sur ce qui se trouve dans l’objet BLOB d’erreurs, consultez la section Notes en bas de cette rubrique.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si cette méthode réussit, la valeur de retour est NMERR \_ Success.

Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants (qui incluent les erreurs retournées par l’appel Internal **IRTC :: configure** ) :



| Code de retour                                                                                                         | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ déjà \_ connecté**</dt> </dl>            | Cette instance de l’objet COM NPP est déjà connectée au réseau.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_erreur de conversion d’objet BLOB NMERR \_ \_**</dt> </dl>       | L’objet BLOB de configuration est endommagé. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**l' \_ entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas**</dt> </dl> | L’objet BLOB d’entrée spécifié par le paramètre *hInputBlob* n’a pas d’entrée nécessaire pour effectuer cette opération. cette erreur peut être générée par l’appel de **IRTC :: Connecter** ou **IRTC :: configure** . Examinez l’objet BLOB d’erreur retourné par *hErrorBlob* pour déterminer quelle entrée est introuvable.<br/> |
| <dl> <dt>**\_objet BLOB NMERR \_ non \_ initialisé**</dt> </dl>        | La fonction **CreateBlob** n’a pas été appelée. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                         |
| <dl> <dt>**\_chaîne d’objet BLOB NMERR \_ \_ non valide**</dt> </dl>         | La chaîne ne se termine pas par un caractère null. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**\_déclencheur NMERR non conforme \_**</dt> </dl>              | La partie déclencheur de l’objet BLOB d’entrée est endommagée. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ \_ objet blob non valide**</dt> </dl>                 | L’objet spécifié dans *hInputBlob* n’est pas un objet BLOB. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ \_ de \_ mémoire insuffisante**</dt> </dl>               | La mémoire nécessaire pour effectuer cette opération n’est pas disponible. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                              |
| <dl> <dt>**\_délai d’expiration de NMERR**</dt> </dl>                       | Le délai d’attente de la demande a expiré. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                                                               |
| <dl> <dt>**NMERR \_ objet blob de niveau supérieur \_**</dt> </dl>                 | Le numéro de version de l’objet BLOB spécifié dans *hInputBlob* est incorrect. Cette erreur est générée par l’appel de **IRTC :: configure** .<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

lorsque la méthode **Connecter** est appelée, le NPP appelle automatiquement la méthode **IRTC :: configure** à l’aide de l’objet BLOB fourni par *hInputBlob*. notez que les codes d’erreur retournés par l’appel à **IRTC :: configure** sont passés en retour et retournés par l’appel de **IRTC :: Connecter** .

Cette méthode doit être appelée avant que vous ne puissiez commencer à capturer des frames. Notez que lorsque vous vous connectez au réseau à l’aide de cette méthode, vous devez continuer à utiliser l’interface **IRTC** pour capturer des frames.

Lorsque vous appelez cette fonction, vous devez spécifier une fonction de rappel d’État ou de frame, même si elle agit uniquement comme un espace réservé.

L’objet BLOB d’entrée spécifié par *hInputBlob* peut être obtenu en appelant les méthodes **GetNPPBlobFromUI**, **GetNPPBlobTable** et **SelectNPPBlobFromTable** .

L’objet BLOB d’erreur retourné dans *hErrorBlob* contient des informations d’erreur que le développeur ou l’application peut utiliser pour la résolution des problèmes. L’objet BLOB d’erreur retourné par *hErrorBlob* contient des entrées que Moniteur réseau n’a pas pu comprendre ou trouver dans l’objet blob d’entrée spécifié dans *hInputBlob*. Par exemple, si \_ l’entrée d’objet BLOB NMERR \_ \_ n' \_ \_ existe pas est retournée, l’entrée Moniteur réseau introuvable est incluse dans l’objet blob d’erreur retourné.



| Pour obtenir des informations sur                          | Consultez                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtention de l’objet BLOB d’entrée qui représente une carte réseau | [Sélection d’une carte d’interface réseau](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC :: configure](irtc-configure.md)
</dt> <dt>

[IRTC ::D éconnecter](irtc-disconnect.md)
</dt> <dt>

[IRTC :: Start](irtc-start.md)
</dt> </dl>

 

 




