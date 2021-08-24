---
title: Définition de modèles de données d’événement
description: Les fournisseurs utilisent des modèles de données pour définir les données spécifiques à l’événement qu’ils incluent avec un événement et pour définir les données de filtre qu’une session de suivi ETW peut passer au fournisseur lorsqu’il active le fournisseur.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5480ca158916801665943bd33b886bfcd5d73015e8730c1dd108123dadc1995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652609"
---
# <a name="defining-event-data-templates"></a>Définition de modèles de données d’événement

Les fournisseurs utilisent des modèles de données pour définir les données spécifiques à l’événement qu’ils incluent avec un événement et pour définir les données de filtre qu’une session de suivi ETW peut passer au fournisseur lorsqu’il active le fournisseur. Si l’événement n’inclut pas de données spécifiques à l’événement, vous ne définissez pas de modèle. Pour définir un modèle, utilisez l’élément **template** . Un modèle contient un élément de données pour chaque élément de données que le fournisseur comprend avec l’événement. Vous pouvez spécifier des types intégraux, des chaînes, des tableaux et des structures. Vous devez écrire les données d’événement dans l’ordre dans lequel les éléments de données ont été définis dans le modèle.

Vous pouvez également inclure dans le modèle, un fragment XML que les consommateurs doivent utiliser pour déterminer comment restituer les données d’événement. Si vous n’incluez pas le fragment, les consommateurs doivent restituer les données d’événement dans l’ordre dans lequel les éléments de données ont été définis dans le modèle.

Lorsque vous définissez un modèle, vous devez lui attribuer un identificateur de modèle que vous utilisez pour référencer le modèle dans une définition d’événement. Chaque élément de données du modèle doit spécifier un nom et un type de données d’entrée (pour obtenir la liste des types d’entrée, consultez la section Notes du type complexe [**InputType**](eventmanifestschema-inputtype-complextype.md) ). Si le type de données d’entrée peut être rendu dans plusieurs formats, vous devez spécifier le type de données de sortie qui indique aux utilisateurs comment restituer l’élément de données. Par exemple, un type de données d’entrée UInt32 peut être rendu sous la forme d’un entier non signé, d’un identificateur de thread, d’une adresse IPv4 et d’un code d’erreur Win32, entre autres. Si vous ne spécifiez pas le type de données de sortie, les consommateurs doivent utiliser le type de sortie par défaut du type d’entrée pour restituer l’élément de données.

Pour spécifier un tableau, incluez l’attribut **Count** sur l’élément de données et affectez-lui le nombre d’éléments dans le tableau. Le tableau peut être un tableau de taille variable ou un tableau de taille fixe. Si le tableau est un tableau de taille fixe, affectez à **Count** la taille du tableau. Par exemple, si un tableau d’entiers a une taille fixe de 10, définissez **Count** sur 10. Lorsque vous écrivez le tableau, vous devez écrire 40 octets de données.

Si le tableau est un tableau de taille variable, définissez **Count** sur le nom de l’élément de données qui contient la taille du tableau. Si le tableau contient des pointeurs, l’adresse des pointeurs est écrite en tant que données d’événement, et non pas les données auxquelles les pointeurs pointent.

Vous devez spécifier l’attribut **Length** si l’élément de données est un objet blob binaire. Vous pouvez également spécifier l’attribut de **longueur** pour les chaînes de longueur fixe.

Spécifiez l’attribut de **mappage** si l’élément de données représente une valeur d’énumération et si vous souhaitez que le consommateur imprime une chaîne pour la valeur au lieu de la valeur elle-même.

Si vous incluez des structures dans le modèle, vous devez écrire les membres de la structure individuellement au lieu d’écrire la structure, sauf si vous pouvez garantir l’alignement de la limite de 8 octets.

Vous devez examiner attentivement les informations que vous incluez dans les événements, en particulier lorsque les événements sont écrits dans les canaux globaux. En règle générale, vous ne devez pas inclure d’informations privées dans les événements. Cela comprend les mots de passe en texte clair et les informations utilisateur personnelles. En outre, les programmes exécutés par l’utilisateur, les URL visitées par l’utilisateur et d’autres informations relatives aux activités de l’utilisateur sur l’ordinateur doivent être considérés comme privés.

si vous devez enregistrer les url et les noms d’utilisateur dans les événements, ne les écrivez pas dans les canaux de Windows (système et Application), car ces canaux sont lisibles par tous les utilisateurs authentifiés. Au lieu de cela, écrivez-les sur vos propres canaux opérationnels ou analytiques. Définissez les autorisations d’accès sur ces canaux pour permettre uniquement aux administrateurs de lire les événements. Vous devrez peut-être fournir une information appropriée pour informer les utilisateurs du fait que des informations privées sont mises à la disposition des administrateurs.

L’exemple suivant montre comment définir un modèle. Vous devez spécifier l’attribut **TID** du modèle que vous référencez dans la définition d’événement ou la définition de filtre.


```XML
<instrumentationManifest
    xmlns="http://schemas.microsoft.com/win/2004/08/events" 
    xmlns:win="http://manifests.microsoft.com/win/2004/08/windows/events"
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    >

    <instrumentation>
        <events>
            <provider name="Microsoft-Windows-SampleProvider"
                guid="{1db28f2e-8f80-4027-8c5a-a11f7f10f62d}"
                symbol="PROVIDER_GUID"
                resourceFileName="<path to the exe or dll that contains the metadata resources>"
                messageFileName="<path to the exe or dll that contains the string resources>"
                message="$(string.Provider.Name)">

                . . .

                <maps>
                    <valueMap name="TransferType">
                        <map value="1" message="$(string.TransferType.Download)"/>
                        <map value="2" message="$(string.TransferType.Upload)"/>
                        <map value="3" message="$(string.TransferType.UploadReply)"/>
                    </valueMap>
                    <bitMap name="DaysOfTheWeek">
                        <map value="0x1" message="$(string.DaysOfTheWeek.Sunday)"/>
                        <map value="0x2" message="$(string.DaysOfTheWeek.Monday)"/>
                        <map value="0x4" message="$(string.DaysOfTheWeek.Tuesday)"/>
                        <map value="0x8" message="$(string.DaysOfTheWeek.Wednesday)"/>
                        <map value="0x10" message="$(string.DaysOfTheWeek.Thursday)"/>
                        <map value="0x20" message="$(string.DaysOfTheWeek.Friday)"/>
                        <map value="0x40" message="$(string.DaysOfTheWeek.Saturday)"/>
                    </bitMap>
                </maps>

                <templates>
                    <template tid="t2">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="Day" inType="win:UInt32" map="DaysOfTheWeek"/>
                        <data name="Transfer" inType="win:UInt32" map="TransferType"/>
                    </template>

                    <template tid="t3">
                        <data name="TransferName" inType="win:UnicodeString"/>
                        <data name="ErrorCode" inType="win:Int32" outType="win:HResult"/>
                        <data name="FilesCount" inType="win:UInt16" />
                        <data name="Files" inType="win:UnicodeString" count="FilesCount"/>
                        <data name="BufferSize" inType="win:UInt32" />
                        <data name="Buffer" inType="win:Binary" length="BufferSize"/>
                        <data name="Certificate" inType="win:Binary" length="11" />
                        <data name="IsLocal" inType="win:Boolean" />
                        <data name="Path" inType="win:UnicodeString" />
                        <data name="ValuesCount" inType="win:UInt16" />
                        <struct name="Values" count="ValuesCount" >
                            <data name="Value" inType="win:UInt16" />
                            <data name="Name" inType="win:UnicodeString" />
                        </struct>
                    </template>
                </templates>

                . . .

            </provider>
        </events>
    </instrumentation>

    <localization>
        <resources culture="en-US">
            <stringTable>
                <string id="Provider.Name" value="Sample Provider"/>
                <string id="TransferType.Download" value="Download"/>
                <string id="TransferType.Upload" value="Upload"/>
                <string id="TransferType.UploadReply" value="Upload-reply"/>
                <string id="DaysOfTheWeek.Sunday" value="Sunday"/>
                <string id="DaysOfTheWeek.Monday" value="Monday"/>
                <string id="DaysOfTheWeek.Tuesday" value="Tuesday"/>
                <string id="DaysOfTheWeek.Wednesday" value="Wednesday"/>
                <string id="DaysOfTheWeek.Thursday" value="Thursday"/>
                <string id="DaysOfTheWeek.Friday" value="Friday"/>
                <string id="DaysOfTheWeek.Saturday" value="Saturday"/>
            </stringTable>
        </resources>
    </localization>

</instrumentationManifest>
```
