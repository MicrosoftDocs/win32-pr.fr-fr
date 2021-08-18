---
title: RasAdminPortClearStatistics, fonction (rassapi. h)
description: La fonction RasAdminPortClearStatistics réinitialise les compteurs représentant les diverses statistiques signalées par la fonction RasAdminPortGetInfo dans la structure des \_ statistiques du port RAS \_ . Les compteurs sont remis à zéro et commencent à s’accumuler.
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da7d17516e7dd7708821a7c60c2d93db913f25c38471524367ae96494e41f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788986"
---
# <a name="rasadminportclearstatistics-function"></a>RasAdminPortClearStatistics fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) .\]

La fonction **RasAdminPortClearStatistics** réinitialise les compteurs représentant les diverses statistiques signalées par la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) dans la structure [**des \_ \_ statistiques du port RAS**](ras-port-statistics-str.md) . Les compteurs sont remis à zéro et commencent à s’accumuler.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du serveur RAS. Spécifiez le nom avec les \\ \\ caractères «» de début, sous la forme : \\ \\ *NomServeur*.

</dd> <dt>

*lpszPort* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne Unicode terminée par le caractère null qui spécifie le nom du port sur le serveur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être le code d’erreur suivant.



| Valeur                                                                                                 | Signification                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**ERREUR \_ de \_ développement \_ inexistant**</dt> </dl> | Le port spécifié n’est pas valide.<br/> |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

La fonction **RasAdminPortClearStatistics** efface les statistiques sur le serveur, pas localement au sein de l’application qui effectue l’appel. Cela signifie que les statistiques sont également réinitialisées pour toute autre application qui surveille le port spécifié.

Si le port *lpszPort* fait partie d’une connexion multilien, **RasAdminPortClearStatistics** réinitialise les statistiques pour le port spécifié, la fonction réinitialise également les statistiques cumulatives pour la connexion à liaisons multiples. Toutefois, la fonction n’affecte pas les statistiques individuelles pour les autres ports qui font partie de la connexion à liaisons multiples.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows 2000 Professionnel<br/>                                                   |
| Fin de la prise en charge des serveurs<br/> | Windows 2000 Server<br/>                                                         |
| En-tête<br/>                | <dl> <dt>Rassapi. h</dt> </dl>   |
| Bibliothèque<br/>               | <dl> <dt>Rassapi. lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Fonctions d’administration du serveur RAS](ras-server-administration-functions.md)
</dt> <dt>

[**\_statistiques du port RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

