---
title: Méthode IWMDRMSecurity PerformSecurityUpdate (wmdrmsdk. h)
description: La méthode PerformSecurityUpdate lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur local.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Méthode PerformSecurityUpdate format Windows Media
- Méthode PerformSecurityUpdate format Windows Media, interface IWMDRMSecurity
- Interface IWMDRMSecurity Windows Media format, méthode PerformSecurityUpdate
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530422"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a>IWMDRMSecurity ::P méthode erformSecurityUpdate

La méthode **PerformSecurityUpdate** lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Option de mise à jour exprimée sous la forme de l’un des indicateurs suivants.



| Indicateur                                          | Description                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| \_sécurité WMDRM \_ exécuter \_ indiv               | Fait en sorte que le composant DRM soit individualisé uniquement si la version du client est obsolète. |
| sécurité WMDRM effectuer l’actualisation de la \_ \_ \_ révocation \_ | Entraîne la mise à jour des listes de révocation sur l’ordinateur client.                               |
| \_forcer la sécurité WMDRM \_ \_ \_ indiv        | Fait en sorte que le composant DRM soit individualisé même si la version du client est à jour.  |



 

</dd> <dt>

*ppunkCancelationCookie* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers un objet qui peut être utilisé pour annuler cette opération.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode s’exécute de façon asynchrone. Elle retourne immédiatement après l’appel de, puis génère des événements en fonction de l’indicateur défini dans le paramètre *dwFlags* .

Pour individualisation (l’indicateur défini sur la \_ sécurité WMDRM \_ perform \_ indiv ou WMDRM \_ Security \_ perform \_ force \_ indiv), une série d’événements **MEWMDRMIndividualizationProgress** est générée, suivie d’un événement **MEWMDRMIndividualizationCompleted** lorsque le traitement est terminé. La valeur de chacun des événements **MEWMDRMIndividualizationProgress** obtenus en appelant **IMFMediaEvent :: GetValue** est un pointeur **IUnknown** . Vous pouvez appeler la méthode **QueryInterface** de l’interface **IUnknown** Récupérée pour récupérer une instance de l’interface [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) .

Pour actualiser les listes de révocation (indicateur défini sur la \_ sécurité WMDRM \_ effectuer l' \_ \_ actualisation), un événement **MEWMDRMREvocationDownloadCompleted** est généré lorsque le traitement est terminé.

> [!Note]  
> Lorsque **PerformSecurityUpdate** termine l’individualisation, les seuls objets existants qui reflètent le nouvel État individualisé sont ceux qui héritent de **IWMDRMSecurity**. Tous les autres objets existants ne seront pas mis à jour. Vous devez libérer et recréer tous les autres objets pour qu’ils reflètent le nouvel État individualisé.

 

Pour plus d’informations sur l’utilisation des méthodes asynchrones des API étendues du client Windows Media DRM, consultez [utilisation du modèle d’événement Media Foundation](using-the-media-foundation-model.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Révocation et renouvellement de composants automatisés**](automated-component-revocation-and-renewal.md)
</dt> <dt>

[**Exemple d’individualisation DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interface IWMDRMSecurity**](iwmdrmsecurity.md)
</dt> <dt>

[**Réalisation de l’individualisation DRM**](performing-drm-individualization.md)
</dt> </dl>

 

 





