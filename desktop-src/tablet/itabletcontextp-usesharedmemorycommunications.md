---
description: Fournit l’accès à la mémoire partagée entre les Tablet threads.
ms.assetid: 047ff598-7d20-49d7-bdd3-498fe5c778c6
title: 'ITabletContextP :: UseSharedMemoryCommunications, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: d7880e1d0377d9d0140a0c82509abd31182c724e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530309"
---
# <a name="itabletcontextpusesharedmemorycommunications-method"></a>ITabletContextP :: UseSharedMemoryCommunications, méthode

Fournit l’accès à la mémoire partagée entre les Tablet threads.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UseSharedMemoryCommunications(
  [in]  DWORD pid,
  [out] DWORD *phEventMoreData,
  [out] DWORD *phEventClientReady,
  [out] DWORD *phMutexAccess,
  [out] DWORD *phFileMapping
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ dans\]
</dt> <dd>

ID de processus.

</dd> <dt>

*phEventMoreData* \[ à\]
</dt> <dd>

Handle d’événement qui signale le moment où de nouvelles données sont disponibles pour être traitées.

</dd> <dt>

*phEventClientReady* \[ à\]
</dt> <dd>

Handle d’événement retourné utilisé pour signaler que le client est prêt à recevoir des données. Signalé après le traitement de nouvelles données.

</dd> <dt>

*phMutexAccess* \[ à\]
</dt> <dd>

Mutex accordant l’accès à la mémoire partagée.

</dd> <dt>

*phFileMapping* \[ à\]
</dt> <dd>

Pointeur vers le bloc de mémoire partagée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                            | Description                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Réussite.<br/>                       |
| <dl> <dt>**E \_ échec**</dt> </dl> | Une erreur non spécifiée s'est produite.<br/> |



 

## <a name="remarks"></a>Notes

La méthode **UseSharedMemoryCommunications** est utilisée dans le cadre du protocole de mémoire partagée du Tablet PC. Étant donné que le service wisptis a un niveau d’intégrité élevé (IL), il peut stocker les données stockées dans la mémoire partagée et y accéder sans avoir à élever ses privilèges.

La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) est convertie à partir des données référencées par le mappage de fichier et les données de paquets brutes suivent l' **\_ en-tête SHAREDMEMORY**. Les données de paquets brutes peuvent être lues à partir de la mémoire partagée lorsque l’événement référencé par *pdwEventClientReady* est déclenché.

La liste suivante décrit la séquence d’événements pour l’accès à et l’utilisation de la mémoire partagée.

-   Le client définit l’événement clientReady.
-   Le client attend l’événement moreData.
-   Le client acquiert le mutex.
-   Le client lit les données de paquets à partir de la section de la mémoire partagée après l’en-tête et les numéros de série après les paquets.
-   Le client gère les données en fonction de la valeur de **dwEvent**.
-   Le client écrit-1 (0xFFFFFFFF) dans **dwEvent**.
-   Le client libère le mutex.
-   Le client définit l’événement clientReady.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface ITabletContextP**](itabletcontextp.md)
</dt> <dt>

[**UseNamedSharedMemoryCommunications**](itabletcontextp-usenamedsharedmemorycommunications.md)
</dt> </dl>

 

 




