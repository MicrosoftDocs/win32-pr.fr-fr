---
title: Méthode IWMDRMSecurity GetContentEnablersForRevocations (wmdrmsdk. h)
description: La méthode GetContentEnablersForRevocations récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Méthode GetContentEnablersForRevocations format Windows Media
- Méthode GetContentEnablersForRevocations format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode GetContentEnablersForRevocations
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532843"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a>IWMDRMSecurity :: GetContentEnablersForRevocations, méthode

La méthode **GetContentEnablersForRevocations** récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rgpbCerts* \[ dans\]
</dt> <dd>

Tableau de certificats pour lequel récupérer des activateurs de contenu. Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*.

</dd> <dt>

*rgpdwCertSizes* \[ dans\]
</dt> <dd>

Tableau contenant les tailles des certificats dans le tableau *rgpbCerts* . Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*.

</dd> <dt>

*rgpguidCerts* \[ dans\]
</dt> <dd>

Tableau contenant les types des certificats dans le tableau *rgpbCerts* . Le nombre d’éléments dans le tableau doit être spécifié par *cCerts*. Pour chaque élément du tableau, utilisez l’une des valeurs suivantes.



| GUID, constante                 | Description                                                    |
|-------------------------------|----------------------------------------------------------------|
| \_application REVOCATIONTYPE \_ WMDRM    | Spécifie un certificat d’application.                          |
| \_appareil REVOCATIONTYPE \_ WMDRM | Spécifie un certificat d’appareil.                                |
| \_REVOCATIONTYPE WMDRM \_ CARDEA | Spécifie un certificat DRM Windows Media pour les périphériques réseau. |



 

</dd> <dt>

*cCerts* \[ dans\]
</dt> <dd>

Nombre de certificats pour lesquels récupérer des activateurs de contenu. Il s’agit du nombre d’éléments dans le tableau *rgpbCerts* , du tableau *rgpdwCertSizes* et du tableau *rgpguidCerts* .

</dd> <dt>

*hResultHint* \[ dans\]
</dt> <dd>

Valeur de retour reçue de l’opération qui a échoué en raison d’un certificat révoqué. Si vous n’appelez pas en réponse à un appel de méthode qui a échoué, définissez sur S \_ OK.

</dd> <dt>

*prgContentEnablers* \[ à\]
</dt> <dd>

Tableau qui reçoit les adresses des interfaces **IMFContentEnabler** nouvellement créées. Affectez la valeur **null** pour récupérer le nombre d’activateurs de contenu dans le paramètre *pcContentEnablers* .

</dd> <dt>

*pcContentEnablers* \[ in, out\]
</dt> <dd>

Nombre d’éléments dans le tableau *prgContentEnablers* . Si *prgContentEnablers* a la valeur **null**, cette valeur est définie sur le nombre d’activateurs de contenu nécessaires sur la sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si vous utilisez l’interface **IMFContentEnabler** pour renouveler des composants révoqués, vous devez clarifier le processus pour l’utilisateur. Cette clarification doit être apportée car le processus de mise à jour envoie des informations de l’ordinateur client vers un site Web Microsoft.

Quand vous appelez **IMFContentEnabler :: AutomaticEnable**, le activateur de contenu lance le navigateur par défaut avec l’adresse du service de mise à jour sur le site Web Microsoft. Un identificateur unique qui identifie le composant révoqué est envoyé au service de mise à jour. Le service redirige ensuite le navigateur vers une page Web à partir de laquelle l’utilisateur peut être en mesure de télécharger et d’installer la nouvelle version du composant révoqué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Révocation et renouvellement de composants automatisés**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> </dl>

 

 





