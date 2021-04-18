---
title: LanguageID, propriété
description: LanguageID, propriété
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311038"
---
# <a name="languageid-property"></a>LanguageID, propriété

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit l’ID de langue pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

Caractères agent. ** ** *  * **(«***CharacterID***»).** \[  =  *LanguageID* LanguageID\]



Partie

Description

LanguageID

Entier long spécifiant l’ID de langue du caractère. L’ID de langue (LANGID) d’un caractère est une valeur de 16 bits définie par Windows, composée d’un ID de langue primaire et d’un ID de langue secondaire. Les exemples suivants sont des valeurs pour les langues prises en charge par Microsoft Agent. Pour déterminer la valeur d’autres langages, consultez la *documentation du kit de développement Platform SDK*.

 

Arabe

&H0401

Italien

&H0410

 

Basque

&H042D

Japonais

&H0411

 

Chinois (simplifié)

&H0804

Coréen

&H0412

 

Chinois (traditionnel)

&H0404

Norvégien

&H0414

 

Croate

&H041A

Polonais

&H0415

 

Tchèque

&H0405

Portugais (Portugal)

&H0816

 

Danois

&H0406

Portugais (Brésil)

&H0416

 

Néerlandais

&H0413

Roumain

&H0418

 

Anglais (Royaume-Uni)

&H0809

Russe

&H0419

 

Anglais (US)

&H0409

Slovaque

&H041B

 

Finnois

&H040B

Slovène

&H0424

 

Français

&H040C

Espagnol

&H0C0A

 

Allemand

&H0407

Suédois

&H041D

 

Grec

&H0408

Thaï

&H041E

 

Hébreu

&H040D

Turc

&H041F

 

Hongrois

&H040E

 

 



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous ne définissez pas l' **LanguageID** pour le caractère, son ID de langue sera l’ID de langue du système actuel si la dll de langue de l’agent correspondante est installée ; sinon, la langue du caractère sera l’anglais (États-Unis).

Cette propriété détermine également la langue du texte de l’info-bulle, les commandes du menu contextuel du caractère et le moteur de reconnaissance vocale. Elle détermine également la langue par défaut de la sortie TTS.

Si vous essayez de définir **LanguageID** pour un caractère et que la dll de langue de l’agent pour cette langue n’est pas installée ou qu’une police d’affichage pour l’ID de langue n’est pas disponible, l’agent génère une erreur et **LanguageID** conserve son dernier paramètre.

La définition de cette propriété ne déclenche pas d’erreur s’il n’existe aucun moteur de reconnaissance vocale correspondant à la langue. Pour déterminer si un moteur vocal compatible est disponible pour **LanguageID**, vérifiez [**SRModeID**](srmodeid-property.md) ou [**TTSModeID**](ttsmodeid-property.md). Si vous ne définissez pas **LanguageID**, il sera défini sur le paramètre ID de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> Si vous affectez à **LanguageID** une langue qui prend en charge le texte bidirectionnel (tel que l’arabe ou l’hébreu), mais que le système qui exécute votre application n’a pas de prise en charge bidirectionnelle, le texte de la bulle est affiché dans l’ordre logique plutôt que dans l’ordre d’affichage.

 

## <a name="see-also"></a>Voir aussi

[**Propriété SRModeID**](srmodeid-property.md), [ **propriété TTSModeID**](ttsmodeid-property.md)


 

 




