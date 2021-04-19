---
title: Propriété SRModeID
description: Propriété SRModeID
ms.assetid: 4c784fc5-d2c2-4e5b-ba5f-f59b4507f40f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898f90a70c29d409eaa12df3d3fde845e35bd5ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511045"
---
# <a name="srmodeid-property"></a>Propriété SRModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le moteur de reconnaissance vocale utilisé par le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). SRModeID* *  \[  =  *ModeID*\]



| Partie     | Description                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expression de chaîne qui correspond à l’ID de mode d’un moteur de reconnaissance vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété détermine le moteur de reconnaissance vocale utilisé par le caractère pour l’entrée vocale. L’ID de mode d’un moteur de reconnaissance vocale est une chaîne mise en forme définie par le fournisseur de reconnaissance vocale qui identifie le moteur de manière unique. Pour plus d’informations, consultez [accès à un moteur de reconnaissance vocale dans votre code](accessing-a-speech-engine-in-your-code.md).

Si vous spécifiez un ID de mode pour un moteur de reconnaissance vocale qui n’est pas installé, si l’utilisateur a désactivé la reconnaissance vocale (dans la feuille de propriétés de l’agent Microsoft), ou si la langue du moteur de reconnaissance vocale spécifié ne correspond pas au paramètre [**LanguageID**](languageid-property.md) du caractère, le serveur génère une erreur.

Si vous interrogez cette propriété et que vous n’avez pas encore défini le moteur de reconnaissance vocale, le serveur retourne l’ID de mode du moteur que SAPI retourne en fonction du paramètre [**LanguageID**](languageid-property.md) du caractère. Si vous n’avez pas défini l’ID de **langue du caractère, agent** retourne l’ID de mode du moteur que SAPI retourne en fonction du paramètre d’ID de langue par défaut de l’utilisateur. S’il n’existe aucun moteur correspondant, le serveur retourne une chaîne vide (""). L’interrogation de cette propriété ne requiert pas que [**SpeechInput. Enabled**](https://www.bing.com/search?q=**SpeechInput.Enabled**) ait la valeur **true**. Toutefois, si vous interrogez la propriété lorsque l’entrée vocale est désactivée, le serveur retourne une chaîne vide.

Lorsque l’entrée vocale est activée (dans la fenêtre Options de caractères avancés), l’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé) et démarrera les services de reconnaissance vocale. Autrement dit, la clé d’écoute est disponible et l’info-bulle d’écoute est affichable. (La clé d’écoute et l’info-bulle d’écoute sont activées uniquement si elles sont également activées dans les options de caractères avancés.) Toutefois, si vous interrogez la propriété alors que la reconnaissance vocale est désactivée, le serveur ne démarre pas les services vocaux.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

> [!Note]  
> Cette propriété retourne également la chaîne vide si aucune prise en charge de son compatible n’est installée sur votre système.

 

> [!Note]  
> L’interrogation de cette propriété ne retourne généralement pas d’erreur. Toutefois, si le temps de chargement du moteur de reconnaissance vocale est anormalement long, vous pouvez obtenir une erreur indiquant que la requête a expiré.

 

## <a name="see-also"></a>Voir aussi

[**LanguageID, propriété**](languageid-property.md)


 

 




