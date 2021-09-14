---
description: La méthode SetBandwidthInfo définit les informations de bande passante.
ms.assetid: bf5db456-ea67-4a65-a681-df0741f73fc9
title: 'ITConnection :: SetBandwidthInfo, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c17054743f6d47775e994dbfe3b80c7afe1ab68
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008744"
---
# <a name="itconnectionsetbandwidthinfo-method"></a>ITConnection :: SetBandwidthInfo, méthode

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetBandwidthInfo** définit les informations de bande passante.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetBandwidthInfo(
  [in] BSTR   pModifier,
  [in] DOUBLE Bandwidth
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pModifier* \[ dans\]
</dt> <dd>

Pointeur vers un **BSTR** indiquant la portée de la bande passante définie. Pour plus d'informations, consultez la section Notes qui suit.

</dd> <dt>

*Bande passante* \[ dans\]
</dt> <dd>

La.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode peut retourner l’une de ces valeurs.



| Valeur                                                                                         | Signification                                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pModifier* ou *Bandwidth* n’est pas valide.<br/> |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>   |
| <dl> <dt>**E \_ échec**</dt> </dl>        | Erreur non spécifiée.<br/>                                     |
| <dl> <dt>**\_NOTIMPL E**</dt> </dl>     | Cette méthode n'est pas encore implémentée.<br/>                    |



 

## <a name="remarks"></a>Notes

L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PModifier* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.

Référence : RFC 2327.

Le modificateur de bande passante sera normalement soit CT, soit :

**Total de la Conférence CT :** Une bande passante maximale implicite est associée à chaque durée de vie (TTL, [*Time to Live*](t-tapgloss.md) ) sur le MBone ou dans une région d’étendue administrative de multidiffusion particulière (les limites de bande passante MBone par rapport à la durée de vie sont indiquées dans le Forum aux questions sur MBone). Si la bande passante d’une session ou d’un support dans une session est différente de la bande passante implicite de l’étendue, un \` b = CT :... la ligne doit être fournie pour la session en donnant la limite supérieure proposée à la bande passante utilisée. L’objectif principal est de fournir une idée approximative du fait que deux conférences ou plus peuvent coexister simultanément.

**Comme Application-Specific maximale :** La bande passante est interprétée comme étant spécifique à l’application, c.-à-d., est le concept de bande passante maximale de l’application. Normalement, cela correspond à ce qui est défini sur le contrôle de « bande passante maximale » de l’application, le cas échéant.

Notez que CT donne une quantité totale de bande passante pour tous les supports sur tous les sites. Tout comme donne une quantité de bande passante pour un seul média sur un seul site, bien qu’il puisse y avoir plusieurs sites envoyant simultanément.

**Mécanisme d’extension :** Les rédacteurs d’outils peuvent définir des modificateurs de bande passante expérimentaux en préfixant leurs modificateurs avec « X- ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

