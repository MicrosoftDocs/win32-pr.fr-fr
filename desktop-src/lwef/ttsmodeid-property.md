---
title: Propriété TTSModeID
description: Propriété TTSModeID
ms.assetid: 9205c37e-e006-466a-9b33-b98408c01ed7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a720b06362b77418434669146a0d89dea8afd37d7a44c4079b2e12c24fcd2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607959"
---
# <a name="ttsmodeid-property"></a>Propriété TTSModeID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le mode de moteur TTS utilisé pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). TTSModeID_ *  \[  =  *ModeID*\]



| Partie     | Description                                                             |
|----------|-------------------------------------------------------------------------|
| *ModeID* | Expression de chaîne qui correspond à l’ID de mode d’un moteur de reconnaissance vocale. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette propriété détermine l’ID de mode de moteur TTS (conversion de texte par synthèse vocale) pour la sortie parlée d’un caractère. L’ID de mode pour un moteur TTS est une chaîne mise en forme définie par le fournisseur de reconnaissance vocale qui identifie de façon unique le mode du moteur. Pour plus d’informations, consultez [accès à un moteur de reconnaissance vocale dans votre code](accessing-a-speech-engine-in-your-code.md).

La définition de cette propriété remplace la tentative du serveur de charger un moteur en fonction du paramètre TTS compilé du caractère et du paramètre [**LanguageID**](languageid-property.md) actuel du caractère. Toutefois, si vous spécifiez un ID de mode pour un moteur qui n’est pas installé ou si l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft (**AudioOutput. Enabled = False**), le serveur génère une erreur.

Si vous ne le faites pas (ou si vous n’avez pas réussi) à définir un ID de mode TTS pour le caractère, le serveur vérifie si le paramètre de mode TTS compilé du caractère correspond au paramètre [**LanguageID**](languageid-property.md) du caractère et que le moteur TTS associé est installé. Si c’est le cas, le mode TTS utilisé par le caractère pour la sortie parlée et cette propriété retourne cet ID de mode. Si ce n’est pas le cas, le serveur demande un moteur de reconnaissance vocale SAPI compatible qui correspond à l’ID de **langue** du caractère, ainsi que le sexe et l’âge définis pour l’ID du mode compilé du caractère. Si vous n’avez pas défini l' **LanguageID** du caractère, son **LanguageID** correspond à la langue de l’utilisateur actuel. Si aucun moteur correspondant n’est trouvé, l’interrogation de cette propriété retourne une chaîne vide pour l’ID de mode du moteur. De même, si vous interrogez cette propriété lorsque l’utilisateur a désactivé la sortie vocale dans la feuille de propriétés de l’agent Microsoft (**AudioOutput. Enabled = False**), la valeur sera une chaîne vide.

L’interrogation ou la définition de cette propriété chargera le moteur associé (s’il n’est pas déjà chargé). Toutefois, si le moteur spécifié dans le paramètre TTS compilé du caractère est installé et correspond au paramètre ID de langue du caractère, le moteur est chargé lorsque le caractère se charge.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

La configuration requise du moteur de reconnaissance vocale de Microsoft Agent est basée sur l’API Microsoft Speech. Les moteurs prenant en charge les spécifications SAPI de Microsoft Agent peuvent être installés et utilisés avec l’agent.

> [!Note]  
> Cette propriété retourne également la chaîne vide si aucune prise en charge de son compatible n’est installée sur votre système.

 

> [!Note]  
> La définition de **TTSModeID** peut échouer si Speech.dll n’est pas installé et que le moteur que vous spécifiez ne correspond pas au paramètre de mode TTS compilé du caractère.

 

> [!Note]  
> L’interrogation de cette propriété ne retourne généralement pas d’erreur. Toutefois, si le temps de chargement du moteur de reconnaissance vocale est anormalement long, vous pouvez obtenir une erreur indiquant que la requête a expiré.

 

## <a name="see-also"></a>Voir aussi

[**LanguageID, propriété**](languageid-property.md)


 

 




