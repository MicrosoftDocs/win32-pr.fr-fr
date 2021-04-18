---
description: Les listes et les tableaux de cette section montrent la sortie du formateur générique. N’oubliez pas que le formateur générique utilise les membres DataType et DataQualifier de la structure PROPERTYINFO pour déterminer comment mettre en forme les données affichées.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Sortie de formateur générique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515975"
---
# <a name="generic-formatter-output"></a>Sortie de formateur générique

Les listes et les tableaux de cette section montrent la sortie du [*formateur générique*](g.md). N’oubliez pas que le formateur générique utilise les membres **DataType** et **DataQualifier** de la structure [**PROPERTYINFO**](propertyinfo.md) pour déterminer comment mettre en forme les données affichées.

Pour plus d’informations et pour obtenir un exemple de sortie pour un type de données de propriété spécifique, consultez :

-   [PROP, \_ type \_ void](/windows)
-   [\_Résumé du type de prop \_](/windows)
-   [\_octet de type prop \_](/windows)
-   [PROP, \_ type \_ Word](/windows)
-   [TYPE de PROP \_ \_ DWORD](/windows)
-   PROP \_ type \_ LARGEINT (le module de formatage générique ne prend pas en charge)
-   PROP \_ type \_ addr (le module de formatage générique ne prend pas en charge)
-   [\_heure du type de prop \_](/windows)
-   [\_chaîne de type prop \_](/windows)
-   [\_ \_ adresse IP du type de prop \_](/windows)
-   PROP \_ type \_ BYTESWAPPED \_ Word (obsolète. Pour plus d’informations, consultez [type de prop, \_ \_ mot](/windows)).
-   PROP \_ type \_ BYTESWAPPED \_ DWORD (obsolète. Pour plus d’informations, consultez [prop, \_ type \_ DWORD](/windows)).
-   \_Type \_ de prop \_ chaîne typée (obsolète)
-   [\_ \_ données brutes de type prop \_](/windows)
-   [Commentaire sur le \_ type prop \_](/windows)
-   PROP \_ type \_ SRCFRIENDLYNAME (le module de formatage générique ne prend pas en charge)
-   PROP \_ type \_ DSTFRIENDLYNAME (le module de formatage générique ne prend pas en charge)
-   PROP \_ type \_ TOKENRING \_ Address (le module de formatage générique ne prend pas en charge)
-   \_Adresse FDDI du type prop (le module \_ \_ de formatage générique ne prend pas en charge)
-   \_Adresse Ethernet du type prop (le module \_ \_ de formatage générique ne prend pas en charge)
-   \_ID d' \_ objet de type prop (le \_ formateur générique ne prend pas en charge)
-   \_ \_ Adresse IP du type de la Vines (le module \_ \_ de formatage générique ne prend pas en charge)
-   PROP \_ type \_ var \_ Len \_ petit \_ int (le module de formatage générique ne prend pas en charge)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ type \_ void et prop \_ type \_ Comment

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données prop et type de **\_ \_ Commentaire** de type prop **\_ \_** .

Dans la colonne de sortie du formateur, la valeur des données de la capture est XYZ.



| Qualificateur de propriété            | Sortie du formateur                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ Qualys \_ None              | XYZ                                                   |
| plage de compétences PROP \_ \_             | XYZ                                                   |
| \_champ de \_ binaire prop Qualys          | Obsolète                                              |
| PROP \_ prop \_ étiquetée \_ Set      | XYZ                                                   |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez les indicateurs de compétences PROPs \_ \_ |
| PROP \_ Qualys \_ const             | XYZ                                                   |
| indicateurs de compétences PROP \_ \_             | XYZ                                                   |
| Tableau de compétences PROP \_ \_             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>\_Résumé du type de prop \_

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données **\_ \_ Summary du type prop** .

Dans l’exemple de colonne de sortie, la valeur des données de la capture est XYZ.



| Qualificateur de propriété            | Exemple de sortie                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ Qualys \_ None              | XYZ                                                   |
| plage de compétences PROP \_ \_             | XYZ                                                   |
| \_champ de \_ binaire prop Qualys          | Obsolète                                              |
| PROP \_ prop \_ étiquetée \_ Set      | XYZ                                                   |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez les indicateurs de compétences PROPs \_ \_ |
| PROP \_ Qualys \_ const             | XYZ                                                   |
| indicateurs de compétences PROP \_ \_             | XYZ                                                   |
| Tableau de compétences PROP \_ \_             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>\_octet de type prop \_

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données **\_ \_ Byte de type prop** .

Dans l’exemple de colonne de sortie, la valeur des données de la capture est 10.



| Qualificateur de propriété            | Exemple de sortie                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ Qualys \_ None              | 10 (0xA) "                                                                                                     |
| plage de compétences PROP \_ \_             | 10 (0xA) plage :(1 (0x1)-20 (0x14))                                                                          |
| ensemble de compétences PROP \_ \_               | 10 (0xA) correspond à la valeur définie ou<br/> 10 (0xA) valeur définie inconnue<br/>                                |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                                                                                     |
| PROP \_ prop \_ étiquetée \_ Set      | Étiquette correspondante dans un jeu d’étiquettes ou un nombre.                                                                 |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ .                                                        |
| PROP \_ Qualys \_ const             | Aucune sortie. Aucune donnée n’est affichée dans le volet d’informations.                                                           |
| indicateurs de compétences PROP \_ \_             | ....... 0 = étiquette de la chaîne...... 1,0. = Étiquette sur la chaîne.... 0.. = Étiqueter la chaîne.... 1... = étiquette sur la chaîne |
| Tableau de compétences PROP \_ \_             | 0A FF...                                                                                                     |



 

## <a name="prop_type_word"></a>PROP, \_ type \_ Word

Le tableau suivant répertorie la sortie de format générique pour une propriété type de données de type **prop \_ \_** .

> [!Note]  
> Pour les propriétés DWORD non-Intel, échangeables par octet, vous devez modifier les données pour qu’elles soient au format Intel. Pour modifier le format, définissez le paramètre *IFlags* de la fonction d’instance de propriété **Attach** IFLAG \_ échangée quand vous mappez l’instance de propriété à un emplacement.

 

Dans l’exemple de colonne de sortie, la valeur des données de la capture est 10.



| Qualificateur de propriété            | Exemple de sortie                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ Qualys \_ None              | 10 (0xA)                                                                                                                                                                                                                      |
| plage de compétences PROP \_ \_             | 10 (0xA) plage :(1 (0x1)-20 (0x14))                                                                                                                                                                                          |
| ensemble de compétences PROP \_ \_               | 10 (0xA) correspond à la valeur définie ou<br/> 10 (0xA) valeur définie inconnue<br/>                                                                                                                                                |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                                                                                                                                                                                                     |
| PROP \_ prop \_ étiquetée \_ Set      | Étiquette correspondante dans le jeu d’étiquettes ou le nombre.                                                                                                                                                                               |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ .                                                                                                                                                                        |
| PROP \_ Qualys \_ const             | Aucune sortie. Aucune donnée n’est affichée dans le volet d’informations.                                                                                                                                                                           |
| indicateurs de compétences PROP \_ \_             | ....... 0 = étiquette de la chaîne...... entre. = Étiqueter la chaîne..... 0.. = Étiqueter la chaîne.... 0... = étiquette de la chaîne... 0.... = étiquette de la chaîne.. 1...... = Étiquette sur String. 0...... = Étiquette de la chaîne 1...... = Étiquette sur la chaîne |
| Tableau de compétences PROP \_ \_             | 000a ffff...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>TYPE de PROP \_ \_ DWORD

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données **\_ \_ DWORD du type prop** .

> [!Note]  
> Pour les propriétés DWORD non-Intel, échangeables par octet, vous devez modifier les données pour qu’elles soient au format Intel. Pour modifier le format, définissez le paramètre *IFlags* de la fonction d’instance de propriété **Attach** IFLAG \_ échangée quand vous mappez l’instance de propriété à un emplacement.

 

Dans l’exemple de colonne de sortie, la valeur des données de la capture est 10.



| Qualificateur de propriété            | Exemple de sortie                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ Qualys \_ None              | 10 (0xA)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| plage de compétences PROP \_ \_             | 10 (0xA) plage :(1 (0x1)-20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ensemble de compétences PROP \_ \_               | 10 (0xA) correspond à la valeur définie ou<br/> 10 (0xA) valeur définie inconnue<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROP \_ prop \_ étiquetée \_ Set      | Étiquette correspondante dans le jeu d’étiquettes ou le nombre.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| PROP \_ Qualys \_ const             | Aucune sortie. Aucune donnée n’est affichée dans le volet d’informations.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| indicateurs de compétences PROP \_ \_             | ............... 0 = étiquette de la chaîne............. entre. = Étiqueter la chaîne............. 0.. = Étiqueter la chaîne............ 0... = étiquette de la chaîne............ 0.... = étiqueter la chaîne.......... 0...... = Étiqueter la chaîne......... 0....... = étiqueter la chaîne........ 0........ = étiqueter la chaîne....... 0........ = Étiqueter la chaîne...... 0.......... = étiqueter la chaîne.... 0............................ 0............ = Étiqueter la chaîne... 0.............................. 1.................................................. = Étiquette de la chaîne 1................... = Étiquette sur la chaîne |
| Tableau de compétences PROP \_ \_             | 0000000a FFFFFFFF...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>\_ \_ données brutes de type prop \_

Le tableau suivant répertorie la sortie de format générique pour une propriété type de données de **\_ \_ \_ données brutes de type prop** . Sachez que la sortie du formateur n’affiche pas les données brutes, mais affiche l’étiquette de la propriété.



| Qualificateur de propriété            | Sortie du formateur |
|-------------------------------|------------------|
| PROP \_ Qualys \_ None              | Étiquette de propriété.  |
| plage de compétences PROP \_ \_             | Étiquette de propriété.  |
| \_champ de \_ binaire prop Qualys          | Étiquette de propriété.  |
| PROP \_ prop \_ étiquetée \_ Set      | Étiquette de propriété.  |
| PROP \_ , \_ étiquette de champ de \_ champ | Étiquette de propriété.  |
| PROP \_ Qualys \_ const             | Étiquette de propriété.  |
| indicateurs de compétences PROP \_ \_             | Étiquette de propriété.  |
| Tableau de compétences PROP \_ \_             | Étiquette de propriété.  |



 

## <a name="prop_type_time"></a>\_heure du type de prop \_

Le tableau suivant répertorie la sortie de format générique pour une propriété de type de données **prop \_ type \_ Time** . Sachez que la sortie mise en forme peut varier en fonction du qualificateur de données de la propriété.

Le formateur générique appelle [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) pour obtenir une heure qui est basée sur l’horloge système de l’ordinateur local.



| Qualificateur de propriété            | Sortie du formateur                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ Qualys \_ None              | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |
| plage de compétences PROP \_ \_             | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                                   |
| PROP \_ prop \_ étiquetée \_ Set      | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ .      |
| PROP \_ Qualys \_ const             | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |
| indicateurs de compétences PROP \_ \_             | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |
| Tableau de compétences PROP \_ \_             | Affiche l’heure système en fonction de l’horloge de l’ordinateur local. |



 

## <a name="prop_type_string"></a>\_chaîne de type prop \_

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données **\_ \_ chaîne de type prop** . Sachez que la sortie du formateur peut varier en fonction du qualificateur de données de la propriété.



| Qualificateur de propriété            | Sortie du formateur                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ Qualys \_ None              | Chaîne attachée.                                       |
| plage de compétences PROP \_ \_             | Chaîne attachée.                                       |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                              |
| PROP \_ prop \_ étiquetée \_ Set      | Chaîne attachée.                                       |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ . |
| PROP \_ Qualys \_ const             | Chaîne attachée.                                       |
| indicateurs de compétences PROP \_ \_             | Chaîne attachée.                                       |
| Tableau de compétences PROP \_ \_             | Chaîne attachée.                                       |



 

## <a name="prop_type_ip_address"></a>\_ \_ adresse IP du type de prop \_

Le tableau suivant répertorie la sortie de format générique pour les propriétés de type de données **\_ \_ \_ adresse IP du type prop** . Sachez que la sortie mise en forme peut varier en fonction du qualificateur de données de propriété de la propriété.

Dans l’exemple de colonne de sortie, la valeur des données de la capture est « 129.65.100.2 ».



| Qualificateur de propriété            | Exemple de sortie                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ Qualys \_ None              | 129.65.100.2                                           |
| plage de compétences PROP \_ \_             | 129.65.100.2                                           |
| \_champ de \_ binaire prop Qualys          | Obsolète.                                              |
| PROP \_ prop \_ étiquetée \_ Set      | 129.65.100.2                                           |
| PROP \_ , \_ étiquette de champ de \_ champ | Obsolète. Pour plus d’informations, consultez Propriétés de PROPs \_ \_ . |
| PROP \_ Qualys \_ const             | 129.65.100.2                                           |
| indicateurs de compétences PROP \_ \_             | 129.65.100.2                                           |
| Tableau de compétences PROP \_ \_             | 129.65.100.2                                           |



 

 

