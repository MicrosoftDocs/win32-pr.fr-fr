---
description: Configure la préférence des fonctionnalités par défaut.
ms.assetid: 0afcb25a-2499-4baa-82ad-0706164e2e72
title: 'IH323LineEx :: SetDefaultCapabilityPreferrence, méthode (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64eb3385edb758529f27f9fb90eb0cce998eca60f202c72a28ba48a5318c6b08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992079"
---
# <a name="ih323lineexsetdefaultcapabilitypreferrence-method"></a>IH323LineEx :: SetDefaultCapabilityPreferrence, méthode

\[**SetDefaultCapabilityPreferrence** n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

La méthode **SetDefaultCapabilityPreferrence** configure la préférence des fonctionnalités par défaut. Les capacités ont un poids par défaut de 100. Si l’application spécifie une pondération plus élevée pour une capacité, elle aura une priorité plus élevée au cours de la négociation H. 245. Si l’application définit le poids d’une capacité sur 0, elle n’est pas utilisée dans la négociation H. 245.

Cette méthode est cumulative. Par exemple, si cette méthode est appelée en premier pour désactiver une fonctionnalité et est à nouveau appelée pour en désactiver une autre, les deux fonctionnalités seront désactivées à la suite de ces deux appels.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefaultCapabilityPreferrence(
  [in] DWORD           dwNumCaps,
  [in] H245_CAPABILITY *pCapabilities,
  [in] DWORD           *pWeights
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwNumCaps* \[ dans\]
</dt> <dd>

Valeur **DWORD** qui contient le nombre de fonctionnalités définies avec cette méthode.

</dd> <dt>

*pCapabilities* \[ dans\]
</dt> <dd>

Tableau de fonctionnalités. Chaque élément du tableau est une valeur [**de \_ capacité h245**](h245-capability.md) .

</dd> <dt>

*pWeights* \[ dans\]
</dt> <dd>

Tableau de poids associé aux fonctionnalités.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode peut retourner l’une de ces valeurs.



| Code de retour                                                                                   | Description                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | La méthode a réussi.<br/>                                                                                                                                                                                                |
| <dl> <dt>**\_OUTOFMEMORY E**</dt> </dl> | La mémoire disponible est insuffisante pour effectuer l’opération.<br/>                                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Le paramètre *pCapabilities* a la **valeur null**, ou le paramètre *pWeights* a la valeur **null**, ou *pCapabilities* et *pWeights* ont la **valeur null**, ou le tableau pCapabilities contient un objet de fonctionnalité H. 245 non valide.<br/> |
| <dl> <dt>**\_pointeur E**</dt> </dl>     | Impossible de lire un élément du tableau *pWeights* ou un élément du tableau *pCapabilities* .<br/>                                                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|---------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                 |
| En-tête<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Bibliothèque<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




