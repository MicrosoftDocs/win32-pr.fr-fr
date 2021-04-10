---
title: Définition de modèles de données d’événement
description: Les fournisseurs utilisent des modèles de données pour définir les données spécifiques à l’événement qu’ils incluent avec un événement et pour définir les données de filtre qu’une session de suivi ETW peut passer au fournisseur lorsqu’il active le fournisseur.
ms.assetid: 064227a2-7ce8-461a-9dc0-7519652e6628
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067230472c8de5ce29145e221c109b3f390f0a6c
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2020
ms.locfileid: "103841981"
---
# <a name="defining-event-data-templates"></a><span data-ttu-id="a91cf-103">Définition de modèles de données d’événement</span><span class="sxs-lookup"><span data-stu-id="a91cf-103">Defining Event Data Templates</span></span>

<span data-ttu-id="a91cf-104">Les fournisseurs utilisent des modèles de données pour définir les données spécifiques à l’événement qu’ils incluent avec un événement et pour définir les données de filtre qu’une session de suivi ETW peut passer au fournisseur lorsqu’il active le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="a91cf-104">Providers use data templates to define the event-specific data that they include with an event and to define the filter data that an ETW tracing session can pass to the provider when it enables the provider.</span></span> <span data-ttu-id="a91cf-105">Si l’événement n’inclut pas de données spécifiques à l’événement, vous ne définissez pas de modèle.</span><span class="sxs-lookup"><span data-stu-id="a91cf-105">If the event does not include event-specific data, you will not define a template.</span></span> <span data-ttu-id="a91cf-106">Pour définir un modèle, utilisez l’élément **template** .</span><span class="sxs-lookup"><span data-stu-id="a91cf-106">To define a template, use the **template** element.</span></span> <span data-ttu-id="a91cf-107">Un modèle contient un élément de données pour chaque élément de données que le fournisseur comprend avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="a91cf-107">A template includes a data item for each piece of data that the provider includes with the event.</span></span> <span data-ttu-id="a91cf-108">Vous pouvez spécifier des types intégraux, des chaînes, des tableaux et des structures.</span><span class="sxs-lookup"><span data-stu-id="a91cf-108">You can specify integral types, strings, arrays, and structures.</span></span> <span data-ttu-id="a91cf-109">Vous devez écrire les données d’événement dans l’ordre dans lequel les éléments de données ont été définis dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="a91cf-109">You must write the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="a91cf-110">Vous pouvez également inclure dans le modèle, un fragment XML que les consommateurs doivent utiliser pour déterminer comment restituer les données d’événement.</span><span class="sxs-lookup"><span data-stu-id="a91cf-110">You can also include in the template, an XML fragment that consumers should use to determine how to render the event data.</span></span> <span data-ttu-id="a91cf-111">Si vous n’incluez pas le fragment, les consommateurs doivent restituer les données d’événement dans l’ordre dans lequel les éléments de données ont été définis dans le modèle.</span><span class="sxs-lookup"><span data-stu-id="a91cf-111">If you do not include the fragment, consumers should render the event data in the order that the data items were defined in the template.</span></span>

<span data-ttu-id="a91cf-112">Lorsque vous définissez un modèle, vous devez lui attribuer un identificateur de modèle que vous utilisez pour référencer le modèle dans une définition d’événement.</span><span class="sxs-lookup"><span data-stu-id="a91cf-112">When you define a template, you must give it a template identifier that you use to reference the template in an event definition.</span></span> <span data-ttu-id="a91cf-113">Chaque élément de données du modèle doit spécifier un nom et un type de données d’entrée (pour obtenir la liste des types d’entrée, consultez la section Notes du type complexe [**InputType**](eventmanifestschema-inputtype-complextype.md) ).</span><span class="sxs-lookup"><span data-stu-id="a91cf-113">Each data item in the template must specify a name and input data type (for a list of input types, see the Remarks section of the [**InputType**](eventmanifestschema-inputtype-complextype.md) complex type).</span></span> <span data-ttu-id="a91cf-114">Si le type de données d’entrée peut être rendu dans plusieurs formats, vous devez spécifier le type de données de sortie qui indique aux utilisateurs comment restituer l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="a91cf-114">If the input data type can be rendered in multiple formats, you should specify the output data type that tells consumers how to render the data item.</span></span> <span data-ttu-id="a91cf-115">Par exemple, un type de données d’entrée UInt32 peut être rendu sous la forme d’un entier non signé, d’un identificateur de thread, d’une adresse IPv4 et d’un code d’erreur Win32, entre autres.</span><span class="sxs-lookup"><span data-stu-id="a91cf-115">For example, an UInt32 input data type can be rendered as an unsigned integer, thread identifier, IPv4 address, and Win32 error code among others.</span></span> <span data-ttu-id="a91cf-116">Si vous ne spécifiez pas le type de données de sortie, les consommateurs doivent utiliser le type de sortie par défaut du type d’entrée pour restituer l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="a91cf-116">If you do not specify the output data type, consumers should use the input type's default output type to render the data item.</span></span>

<span data-ttu-id="a91cf-117">Pour spécifier un tableau, incluez l’attribut **Count** sur l’élément de données et affectez-lui le nombre d’éléments dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="a91cf-117">To specify an array, include the **count** attribute on the data item and set it to the number of elements in the array.</span></span> <span data-ttu-id="a91cf-118">Le tableau peut être un tableau de taille variable ou un tableau de taille fixe.</span><span class="sxs-lookup"><span data-stu-id="a91cf-118">The array can be a variable size array or fixed size array.</span></span> <span data-ttu-id="a91cf-119">Si le tableau est un tableau de taille fixe, affectez à **Count** la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="a91cf-119">If the array is a fixed size array, set **count** to the size of the array.</span></span> <span data-ttu-id="a91cf-120">Par exemple, si un tableau d’entiers a une taille fixe de 10, définissez **Count** sur 10.</span><span class="sxs-lookup"><span data-stu-id="a91cf-120">For example, if an array of integers has a fixed size of 10, set **count** to 10.</span></span> <span data-ttu-id="a91cf-121">Lorsque vous écrivez le tableau, vous devez écrire 40 octets de données.</span><span class="sxs-lookup"><span data-stu-id="a91cf-121">When you write the array, you must write 40 bytes of data.</span></span>

<span data-ttu-id="a91cf-122">Si le tableau est un tableau de taille variable, définissez **Count** sur le nom de l’élément de données qui contient la taille du tableau.</span><span class="sxs-lookup"><span data-stu-id="a91cf-122">If the array is a variable size array, set **count** to the name of the data item that contains the size of the array.</span></span> <span data-ttu-id="a91cf-123">Si le tableau contient des pointeurs, l’adresse des pointeurs est écrite en tant que données d’événement, et non pas les données auxquelles les pointeurs pointent.</span><span class="sxs-lookup"><span data-stu-id="a91cf-123">If the array contains pointers, the address of the pointers are written as the event data, not the data to which the pointers point.</span></span>

<span data-ttu-id="a91cf-124">Vous devez spécifier l’attribut **Length** si l’élément de données est un objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="a91cf-124">You must specify the **length** attribute if the data item is a binary blob.</span></span> <span data-ttu-id="a91cf-125">Vous pouvez également spécifier l’attribut de **longueur** pour les chaînes de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="a91cf-125">You can also specify the **length** attribute for fixed length strings.</span></span>

<span data-ttu-id="a91cf-126">Spécifiez l’attribut de **mappage** si l’élément de données représente une valeur d’énumération et si vous souhaitez que le consommateur imprime une chaîne pour la valeur au lieu de la valeur elle-même.</span><span class="sxs-lookup"><span data-stu-id="a91cf-126">Specify the **map** attribute if the data item represents an enumeration value and you want the consumer to print a string for the value instead of the value itself.</span></span>

<span data-ttu-id="a91cf-127">Si vous incluez des structures dans le modèle, vous devez écrire les membres de la structure individuellement au lieu d’écrire la structure, sauf si vous pouvez garantir l’alignement de la limite de 8 octets.</span><span class="sxs-lookup"><span data-stu-id="a91cf-127">If you include structures in the template, you should write the members of the structure individually instead of writing the structure unless you can guarantee 8-byte boundary alignment.</span></span>

<span data-ttu-id="a91cf-128">Vous devez examiner attentivement les informations que vous incluez dans les événements, en particulier lorsque les événements sont écrits dans les canaux globaux.</span><span class="sxs-lookup"><span data-stu-id="a91cf-128">You should carefully consider the information that you include in the events, especially when the events are written into the global channels.</span></span> <span data-ttu-id="a91cf-129">En règle générale, vous ne devez pas inclure d’informations privées dans les événements.</span><span class="sxs-lookup"><span data-stu-id="a91cf-129">As a general rule, you should not include private information in the events.</span></span> <span data-ttu-id="a91cf-130">Cela comprend les mots de passe en texte clair et les informations utilisateur personnelles.</span><span class="sxs-lookup"><span data-stu-id="a91cf-130">This includes plaintext passwords and personal user information.</span></span> <span data-ttu-id="a91cf-131">En outre, les programmes exécutés par l’utilisateur, les URL visitées par l’utilisateur et d’autres informations relatives aux activités de l’utilisateur sur l’ordinateur doivent être considérés comme privés.</span><span class="sxs-lookup"><span data-stu-id="a91cf-131">Additionally, programs run by the user, URLs that the user visited, and other information related to the user activities on the computer should be considered private.</span></span>

<span data-ttu-id="a91cf-132">Si vous devez enregistrer les URL et les noms d’utilisateur dans les événements, ne les écrivez pas sur les canaux Windows (système et application), car ces canaux sont lisibles par tous les utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="a91cf-132">If you must record URLs and user names in the events, do not write them to the Windows channels (System and Application) because these channels are readable by all authenticated users.</span></span> <span data-ttu-id="a91cf-133">Au lieu de cela, écrivez-les sur vos propres canaux opérationnels ou analytiques.</span><span class="sxs-lookup"><span data-stu-id="a91cf-133">Instead, write them to your own Operational or Analytic channels.</span></span> <span data-ttu-id="a91cf-134">Définissez les autorisations d’accès sur ces canaux pour permettre uniquement aux administrateurs de lire les événements.</span><span class="sxs-lookup"><span data-stu-id="a91cf-134">Set the access permissions on these channels to allow only administrators to read the events.</span></span> <span data-ttu-id="a91cf-135">Vous devrez peut-être fournir une information appropriée pour informer les utilisateurs du fait que des informations privées sont mises à la disposition des administrateurs.</span><span class="sxs-lookup"><span data-stu-id="a91cf-135">You may need to provide an appropriate disclosure to notify users of the fact that private information is made available to the administrators.</span></span>

<span data-ttu-id="a91cf-136">L’exemple suivant montre comment définir un modèle.</span><span class="sxs-lookup"><span data-stu-id="a91cf-136">The following example shows how to define a template.</span></span> <span data-ttu-id="a91cf-137">Vous devez spécifier l’attribut **TID** du modèle que vous référencez dans la définition d’événement ou la définition de filtre.</span><span class="sxs-lookup"><span data-stu-id="a91cf-137">You must specify the template's **tid** attribute that you reference in the event definition or filter definition.</span></span>


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
