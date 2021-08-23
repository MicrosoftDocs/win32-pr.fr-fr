---
description: Configure la communication de la mémoire partagée pour le contexte de la tablette.
ms.assetid: 63e6b271-d89a-4c91-9a15-9e41dcdfa363
title: 'ITabletContextP :: UseNamedSharedMemoryCommunications, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.UseNamedSharedMemoryCommunications
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: a8ce5d4dde7f3fd678e4ac748a0f148750344a1e5e8da9f6481ad25eafa016a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119712229"
---
# <a name="itabletcontextpusenamedsharedmemorycommunications-method"></a>ITabletContextP :: UseNamedSharedMemoryCommunications, méthode

Configure la communication de la mémoire partagée pour le contexte de la tablette.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT UseNamedSharedMemoryCommunications(
  [in]  DWORD  pid,
  [in]  LPCSTR pszCallerSid,
  [in]  LPCSTR pszCallerIntegritySid,
  [out] DWORD  *pdwEventMoreDataId,
  [out] DWORD  *pdwEventClientReadyId,
  [out] DWORD  *pdwMutexAccessId,
  [out] DWORD  *pdwFileMappingId
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PID* \[ dans\]
</dt> <dd>

ID de processus du client qui accède à la mémoire partagée.

</dd> <dt>

*pszCallerSid* \[ dans\]
</dt> <dd>

Identificateur de sécurité de l’appelant de la fonction.

</dd> <dt>

*pszCallerIntegritySid* \[ dans\]
</dt> <dd>

Identificateur de sécurité qui peut vérifier l’intégrité de la fonction appelante.

</dd> <dt>

*pdwEventMoreDataId* \[ à\]
</dt> <dd>

Entier utilisé pour construire le nom d’un événement. L’événement indique s’il y a plus de données.

</dd> <dt>

*pdwEventClientReadyId* \[ à\]
</dt> <dd>

Entier utilisé pour construire le nom d’un événement. L’événement signale que le client est prêt à recevoir des données. L’événement est signalé après le traitement de nouvelles données.

</dd> <dt>

*pdwMutexAccessId* \[ à\]
</dt> <dd>

Pointeur vers l’identificateur d’accès de la mémoire partagée.

</dd> <dt>

*pdwFileMappingId* \[ à\]
</dt> <dd>

Entier qui identifie la mémoire partagée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

La méthode **UseNamedSharedMemoryCommunications** fait partie du protocole de mémoire partagée du Tablet PC. Un client sans privilèges élevés passe dans un identificateur de sécurité (SID) et un identificateur de sécurité de niveau d’intégrité (IL-SID) afin que le service tablette puisse utiliser des listes de contrôle d’accès (ACL) pour accéder aux objets de mémoire partagée. Si le client dispose de privilèges élevés, il doit utiliser UseSharedMemoryCommunications, qui est l’API appelée si le service a déjà un privilège élevé.

La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) stocke l’en-tête de mémoire partagée.

La structure d' [**\_ en-tête SHAREDMEMORY**](sharedmemory-header.md) est convertie à partir des données référencées par le mappage de fichier. Les données de paquets brutes suivent l' **\_ en-tête SHAREDMEMORY**. Les données de paquets brutes peuvent être lues à partir de la mémoire partagée lorsque l’événement référencé par *pdwEventClientReadyId* est déclenché.

La liste suivante décrit la séquence d’événements pour l’accès à et l’utilisation de la mémoire partagée.

1.  Le client déclenche l’événement clientReady.
2.  Le client attend l’événement moreData.
3.  Le client acquiert le mutex.
4.  Le client lit les données de paquets à partir de la section de la mémoire partagée qui suit l’en-tête. Les numéros de série s’affichent dans la mémoire partagée après les données du paquet.
5.  Le client gère les données en fonction de la valeur de **dwEvent**.
6.  Le client écrit-1 (0xFFFFFFFF) dans **dwEvent**.
7.  Le client libère le mutex.
8.  Le client déclenche l’événement clientReady.

Les noms d’événements sont créés en mettant en forme la sortie de cette méthode. Les définitions suivantes peuvent être utilisées conjointement avec sprintf ou son équivalent pour créer les noms d’événements.


```C++
#define WISPTIS_SM_MORE_DATA_EVENT_NAME     _T("wisptis-1-%d-%u")
#define WISPTIS_SM_CLIENT_DONE_EVENT_NAME   _T("wisptis-2-%d-%u")
#define WISPTIS_SM_SECTION_NAME             _T("wisptis-3-%d-%u")
#define WISPTIS_SM_THREAD_EVENT_NAME        _T("wisptis-4-%u")
```



Dans chaque définition, la section% d est remplacée par l’ID de processus, et la section% u est remplacée par l’entier retourné dans *pdwEventMoreDataId* ou *pdwEventClientReadyId*.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Bibliothèque<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**UseSharedMemoryCommunications**](itabletcontextp-usesharedmemorycommunications.md)
</dt> <dt>

[**ITabletContextP**](itabletcontextp.md)
</dt> </dl>

 

 




