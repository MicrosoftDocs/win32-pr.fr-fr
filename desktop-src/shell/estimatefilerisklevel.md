---
description: Estime le risque d’exécution de code inconnu lorsqu’un gestionnaire est appelé sur un fichier donné. Ce risque est basé sur une compréhension du gestionnaire et le contenu du code du fichier.
title: EstimateFileRiskLevel fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 96798e0bc64b39ae7f18d58b97fafafc9dc2508b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973615"
---
# <a name="estimatefilerisklevel-function"></a>EstimateFileRiskLevel fonction)

\[Cette fonction est disponible sur Windows XP avec Service Pack 2 (SP2) par le biais de Windows Vista. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. À la place, les applications clientes doivent utiliser [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) pour présenter un environnement utilisateur qui permet de télécharger et d’échanger des fichiers en toute sécurité via des pièces jointes de messagerie électronique et de messagerie.\]

Estime le risque d’exécution de code inconnu lorsqu’un gestionnaire est appelé sur un fichier donné. Ce risque est basé sur une compréhension du gestionnaire et le contenu du code du fichier.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszFilePath* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès du fichier qui est vérifié par rapport au gestionnaire.

</dd> <dt>

*pszExt* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne terminée par le caractère null qui contient l’extension du fichier qui est vérifié, avec ou sans son point de début. Par exemple, « . txt » ou « txt ».

</dd> <dt>

*pszHandler* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une chaîne se terminant par un caractère null qui contient le chemin d’accès du gestionnaire pour le fichier.

</dd> <dt>

*pfrlEstimate* \[ à\]
</dt> <dd>

Type : **fichier \_ \_ niveau \* de risque* _

Lorsque cette fonction est retournée avec succès, contient un pointeur vers l’une des valeurs suivantes qui indique le risque estimé.

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>_ *FRL \_ aucun \_ avis** (0)


</dt> <dd>

Le format du fichier n’est pas identifié ou le gestionnaire n’est pas identifié. Informations insuffisantes pour obtenir une réponse pertinente.

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_ FAIBLE** (1)


</dt> <dd>

Le format du fichier est entièrement compris, le gestionnaire est connu et il est très sûr qu’aucun code superflu ne soit exécuté.

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_ MODÉRÉ** (2)


</dt> <dd>

Le format du fichier est identifié, mais il n’est pas suffisamment compréhensible pour l’étiquetage comme un risque élevé ou faible.

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_ ÉLEVÉ** (3)


</dt> <dd>

Le format de fichier est compris et les facteurs de risque élevés ont été identifiés.

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_ BLOC** (4)


</dt> <dd>

Le format de fichier est spécifiquement bloqué pour ce gestionnaire.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette fonction n’est pas déclarée dans un en-tête public ou incluse dans un fichier de bibliothèque. Pour l’utiliser, vous devez la charger directement à partir de Winshfhc.dll par l’ordinal 101.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP2 uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (version 5,1 ou ultérieure)</dt> </dl> |



 

 




