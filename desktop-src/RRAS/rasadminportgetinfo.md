---
title: RasAdminPortGetInfo, fonction (rassapi. h)
description: La fonction RasAdminPortGetInfo récupère des informations sur un port spécifié sur un serveur spécifié.
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo fonction RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522822"
---
# <a name="rasadminportgetinfo-function"></a>RasAdminPortGetInfo fonction)

\[Cette fonction est fournie uniquement pour la compatibilité descendante avec Windows NT Server 4,0. Elle retourne un \_ appel \_ d’erreur non \_ implémenté sur Windows Server 2003. Les applications doivent utiliser la fonction [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) .\]

La fonction **RasAdminPortGetInfo** récupère des informations sur un port spécifié sur un serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
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

</dd> <dt>

*pRasPort1* \[ à\]
</dt> <dd>

Pointeur vers la structure du [**\_ port \_ 1 RAS**](ras-port-1-str.md) que la fonction remplit à l’aide d’informations sur l’état du port.

</dd> <dt>

*pRasStats* \[ à\]
</dt> <dd>

Pointeur vers la structure des [**\_ \_ statistiques du port RAS**](ras-port-statistics-str.md) que la fonction remplit avec des statistiques sur le port.

</dd> <dt>

*ppRasParams* \[ à\]
</dt> <dd>

Pointeur vers une variable pointeur qui reçoit l’adresse d’un tableau de structures de [**\_ paramètres RAS**](ras-parameters-str.md) . Chaque structure contient le nom d’une clé spécifique au support, par exemple MAXCONNECTBPS, et sa valeur associée. Lorsque l’application a terminé cette mémoire, libérez-la en appelant la fonction [**RasAdminFreeBuffer**](rasadminfreebuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes d’erreur suivants.



| Valeur                                                                                                     | Signification                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**ERREUR \_ de \_ développement \_ inexistant**</dt> </dl>     | Le port spécifié n’est pas valide.<br/>                                        |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl> | Mémoire insuffisante pour allouer une mémoire tampon pour le tableau *ppRasParams* .<br/> |



 

Il n’y a pas d’informations d’erreur étendues pour cette fonction. ne pas appeler [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

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

[**\_paramètres RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_Port RAS \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**\_statistiques du port RAS \_**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

