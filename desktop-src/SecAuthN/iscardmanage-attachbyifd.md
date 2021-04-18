---
description: Crée un lien de communication vers un lecteur, à l’aide d’un nom d’affichage fourni pour le lecteur.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'ISCardManage :: AttachByIFD, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522709"
---
# <a name="iscardmanageattachbyifd-method"></a>ISCardManage :: AttachByIFD, méthode

\[La méthode **AttachByIFD** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Il n’est pas disponible pour une utilisation dans Windows Server 2003 avec Service Pack 1 (SP1) et versions ultérieures, Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. Les [modules de carte à puce](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrent des fonctionnalités similaires.\]

La méthode **AttachByIFD** crée un lien de communication vers un [*lecteur*](../secgloss/r-gly.md), à l’aide d’un nom d’affichage fourni pour le lecteur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrIFDName* \[ dans\]
</dt> <dd>

Nom complet du lecteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne l’une des valeurs possibles suivantes :



| Code de retour                                                                                   | Description                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Opération exécutée avec succès.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *bstrIFDName* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | Mémoire insuffisante.<br/>                            |



 

## <a name="remarks"></a>Notes

Pour joindre un appel de [*carte à puce*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).

Pour libérer le [**détachement**](iscardmanage-detach.md)d’un appel de pièce jointe.

Pour vous reconnecter à la carte à puce sans appeler [**Detach**](iscardmanage-detach.md) et **AttachByIFD**, appelez [**reconnect**](iscardmanage-reconnect.md).

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

[**Dissocié**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Reconnexion**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
