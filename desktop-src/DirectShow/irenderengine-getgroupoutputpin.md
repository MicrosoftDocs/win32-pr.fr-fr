---
description: La méthode GetGroupOutputPin récupère la broche de sortie pour le groupe spécifié.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine :: GetGroupOutputPin, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006602"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>IRenderEngine :: GetGroupOutputPin, méthode

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

La `GetGroupOutputPin` méthode récupère la broche de sortie pour le groupe spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Groupe* 
</dt> <dd>

Index de base zéro qui spécifie le groupe.

</dd> <dt>

*ppRenderPin* \[ à\]
</dt> <dd>

Reçoit un pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) de la broche de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **HRESULT** . Il peut prendre les valeurs suivantes :



| Code de retour                                                                                                  | Description                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Le groupe n’a pas de broche de sortie.<br/>                              |
| <dl> <dt>**\_OK**</dt> </dl>                         | Réussite.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argument non valide.<br/>                                               |
| <dl> <dt>**E \_ doit \_ initialiser le \_ convertisseur**</dt> </dl>       | Le moteur de rendu n’a pas pu s’initialiser.<br/>                             |
| <dl> <dt>**\_pointeur E**</dt> </dl>                    | Pointeur non valide.<br/>                                                |
| <dl> <dt>**le \_ moteur de rendu E \_ \_ est \_ défectueux**</dt> </dl> | L’opération a échoué, car le projet n’a pas été rendu correctement.<br/> |
| <dl> <dt>**E \_ inattendu**</dt> </dl>                 | Erreur inattendue.<br/>                                               |



 

## <a name="remarks"></a>Notes

Avant d’appeler cette méthode, appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique. Chaque groupe représente un flux de données multimédia unique et le serveur frontal a une broche de sortie correspondante.

Vous pouvez utiliser cette méthode pour créer la partie de rendu d’un graphique d’écriture de fichiers. Connecter les broches de sortie aux filtres de multiplexeur et aux filtres du writer de fichier. Pour plus d’informations, consultez [rendu d’un Project](rendering-a-project.md).

Pour la version préliminaire, vous n’avez pas besoin d’appeler cette méthode. Appelez simplement **ConnectFrontEnd** suivi de [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md).

Si la méthode retourne la valeur \_ OK, l’interface **IPIN** qu’elle retourne a un nombre de références en attente. Veillez à libérer l’interface une fois que vous avez fini de l’utiliser.

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




