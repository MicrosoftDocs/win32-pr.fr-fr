---
description: Permet à une application de se reconnecter à une carte à puce ou à un lecteur sans avoir à émettre un appel de détachement suivi par un appel de AttachByHandle ou AttachByIFD, respectivement.
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: 'ISCardManage :: reconnect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: b8b05e6292a92267569eb1f53e10f6143554aba1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864046"
---
# <a name="iscardmanagereconnect-method"></a>ISCardManage :: reconnect, méthode

\[La méthode de **reconnexion** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **reconnect** permet à une application de se reconnecter à une [*carte à puce*](../secgloss/s-gly.md) ou à un [*lecteur*](../secgloss/r-gly.md) sans avoir à émettre un appel de [**détachement**](iscardmanage-detach.md) suivi d’un appel [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md) , respectivement.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                    |



 

## <a name="remarks"></a>Notes

Pour joindre un appel de carte à puce [**AttachByHandle**](iscardmanage-attachbyhandle.md) ou [**AttachByIFD**](iscardmanage-attachbyifd.md).

Pour détacher une carte à puce, appelez [**détacher**](iscardmanage-detach.md).

Pour obtenir la liste de toutes les méthodes définies par cette interface, consultez [**ISCardManage**](iscardmanage.md).

Outre les codes d’erreur COM listés ci-dessus, cette interface peut retourner un code d’erreur de carte à puce si une fonction de carte à puce a été appelée pour terminer la demande. Pour plus d’informations, consultez [valeurs de retour de carte à puce](authentication-return-values.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Dissocié**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
