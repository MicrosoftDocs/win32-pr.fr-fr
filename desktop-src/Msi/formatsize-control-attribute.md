---
description: Si ce bit est défini pour un contrôle de texte statique, le contrôle essaie automatiquement de mettre en forme le texte affiché sous la forme d’un nombre qui représente un nombre d’octets.
ms.assetid: acf76fff-b7a4-456b-91b9-eb3087879d7b
title: Formater l’attribut de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7fa656b81272b8ac60985d3dac0416c0f81bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201959"
---
# <a name="formatsize-control-attribute"></a>Formater l’attribut de contrôle

Si ce bit est défini pour un contrôle de texte statique, le contrôle essaie automatiquement de mettre en forme le texte affiché sous la forme d’un nombre qui représente un nombre d’octets. Pour une mise en forme appropriée, le texte du contrôle doit être défini sur une chaîne qui représente un nombre exprimé en unités de 512 octets. La valeur affichée est ensuite exprimée en kilo-octets (Ko), mégaoctets (Mo) ou gigaoctets (Go) et affichée avec la chaîne appropriée qui représente les unités. Pour plus d’informations, consultez [contrôle de texte](text-control.md).



| Valeur numérique du texte d’origine | Chaîne d’unité utilisée |
|----------------------------------|------------------|
| Inférieur à 20480                  | Ko               |
| Inférieur à 20971520               | Mo               |
| Inférieur à 10737418240            | Go               |



 

## <a name="valid-controls"></a>Contrôles valides



| Decimal | Valeur hexadécimale | Contrôler                          |
|---------|-------------|----------------------------------|
| 524 288  | 0x00080000  | msidbControlAttributesFormatSize |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez les bits de format dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md). Le texte du contrôle doit être défini sur une chaîne représentant un nombre exprimé en unités de 512 octets. Le texte des chaînes d’unité est défini dans la [table UIText](uitext-table.md). Le positionnement de la chaîne d’unité est contrôlé par la propriété [**LeftUnit**](leftunit.md) . Si la propriété **LeftUnit** est définie comme n’importe quelle valeur, la chaîne d’unité apparaît avant la valeur numérique. Si tout autre caractère numérique apparaît dans le texte associé au contrôle, la valeur affichée n’est pas définie.

Au moment de l’exécution, le programme d’installation résout la valeur de la propriété [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) sur le nombre total d’octets requis pour l’installation, en unités de 512. Un contrôle de texte statique avec le bit de mise en forme peut être utilisé pour mettre automatiquement en forme et étiqueter le nombre total d’octets requis pour l’installation, en Ko, Mo ou Go, selon le cas. Dans le cadre de cet exemple, supposons que le nombre total d’octets est 18 336 768. Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRequired sur 18 336 768 divisée par 512, ou 35 814. Le nombre affiché par le contrôle de texte avec la fonction de formatage est 17MB.

Les valeurs numériques du texte d’origine sont indiquées en unités de 512. Dans le tableau ci-dessus, la chaîne 20 480 correspond à la chaîne de base de connaissances, car 20 480 fois 512 produit un résultat de 10 485 760 octets ou de 10 240 Ko.

Les chaînes d’unités listées dans le tableau précédent font référence aux clés de la [table UIText](uitext-table.md), où le texte de la chaîne d’unité est défini.

Le positionnement de la chaîne d’unité est contrôlé par la propriété [**LeftUnit**](leftunit.md) . Si la propriété **LeftUnit** est définie comme n’importe quelle valeur, la chaîne d’unité apparaît avant la valeur numérique.

Si tout autre caractère numérique apparaît dans le texte associé au contrôle, la valeur affichée n’est pas définie.

Pour plus d’informations, consultez [contrôles](controls.md)et [attributs](control-attributes.md) .

 

 



