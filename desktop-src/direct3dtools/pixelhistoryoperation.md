---
description: Représente des informations sur l’historique des pixels.
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryOperation, structure
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517380"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation, structure

Représente des informations sur l’historique des pixels.

## <a name="syntax"></a>Syntaxe


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>Membres

**Numéro**  
ID de l’événement graphique associé à cette opération.

**PCP**  
Appels empaquetés associés à cette opération.

**renderTargetPtr**  
Cible de rendu associée à l’origine (à l’intérieur de l’application capturée) avec cette opération.

**iPrim**  
Index de la primitive réelle associée à son opération.

**numPrims**  
Nombre total de primitives associées à cette opération.

**numVertsPerPrim**  
Nombre de vertex par primitive.

**iInstance**  
Lors du rendu des instances, le numéro d’instance de l’instance réelle associée à cette opération.

**iInstanceCount**  
Lors du rendu des instances, nombre total d’instances associées à cette opération.

**bAssemblerStageGeneratesInstanceID**  
true si l’assembleur d’entrée génère des ID d’instance ; Sinon, false.

**flags**  
Combinaison de valeurs PIXELHISTORYFLAGS. Pour plus d’informations, consultez l’énumération PIXELHISTORYFLAGS.

**pVSFile**  
FILEPTR pour le flux d’octets du nuanceur de pixels. Cette valeur est retournée pour déboguer.

**pGSFile**  
FILEPTR pour le flux d’octets du nuanceur Geometry. Cette valeur est retournée pour déboguer.

**pPSFile**  
FILEPTR pour le flux d’octets du nuanceur de pixels. Cette valeur est retournée pour déboguer.

**pHSFile**  
FILEPTR pour le flux d’octets du nuanceur de coque. Cette valeur est retournée pour déboguer.

**pDSFile**  
FILEPTR pour le flux d’octets du nuanceur de domaine. Cette valeur est retournée pour déboguer.

**pCSFile**  
FILEPTR pour le flux d’octets du nuanceur de calcul. Cette valeur est retournée pour déboguer.

**VertexShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de sommets.

**PixelShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de pixels.

**GeometryShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur Geometry.

**HullShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de coque.

**DomainShaderFile**  
Chaîne COM contenant le chemin d’accès du fichier source du nuanceur de domaine.

**psRed**  
Sortie du nuanceur de pixels : valeur du composant de couleur rouge.

**psGreen**  
Sortie du nuanceur de pixels : valeur du composant de couleur verte.

**psBlue**  
Sortie du nuanceur de pixels : valeur du composant de couleur bleu

**psAlpha**  
Sortie du nuanceur de pixels : valeur du composant de couleur alpha

**LabelPSRed**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge de la sortie du nuanceur de pixels.

**LabelPSGreen**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte de la sortie du nuanceur de pixels.

**LabelPSBlue**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu de la sortie du nuanceur de pixels.

**LabelPSAlpha**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha de la sortie du nuanceur de pixels.

**pixelKillReason**  
Sortie du nuanceur de pixels : raison pour laquelle la sortie de pixel a été arrêtée.

**pixelOccluded**  
true si le pixel est bloqués ; Sinon, false.

**fbRed**  
Trame : la valeur du composant de couleur rouge de trame avant la sortie du nuanceur de pixels est fusionnée.

**fbGreen**  
Trame : la valeur du composant de couleur verte de trame avant la sortie du nuanceur de pixels est fusionnée.

**fbBlue**  
Trame : la valeur du composant de couleur bleu de trame avant la sortie du nuanceur de pixels est fusionnée.

**fbAlpha**  
Trame : la valeur du composant de couleur alpha de trame avant la sortie du nuanceur de pixels est fusionnée.

**LabelFBRed**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur rouge du trame.

**LabelFBGreen**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur verte du trame.

**LabelFBBlue**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur bleu du trame.

**LabelFBAlpha**  
Chaîne COM contenant le nom de l’étiquette associée au composant de couleur alpha du trame.

**topologie**  
Topologie de vertex des appels de dessin (liste de triangles, bande triangulaire, etc.).

**derniers**  
Chaîne COM contenant la mémoire tampon de vertex en commençant à cette primitive. La mémoire tampon de vertex suit le format de disposition d’entrée spécifié dans l’étape de pipeline.

**vertexSize**  
Taille d’un seul vertex en octets.

**InputLayout**  
Chaîne COM contenant une séquence de structures InputLayoutStruct associées à l’appel de dessin.

**HResult**  
HRESULT DirectX. En cas de problème, vous pouvez l’utiliser pour afficher l’erreur.

## <a name="requirements"></a>Configuration requise

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>En-tête</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



