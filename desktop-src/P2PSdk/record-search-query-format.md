---
description: Un appel à la fonction PeerGroupSearchRecords nécessite un paramètre de chaîne de requête XML utilisé pour déterminer les critères de base d’une recherche.
ms.assetid: 2c5ab425-6959-418a-8d9a-c8155257fc7e
title: Format de requête de recherche d’enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b475c8a449e3bcd360df5757fef508b1a744d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867006"
---
# <a name="record-search-query-format"></a><span data-ttu-id="422e4-103">Format de requête de recherche d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="422e4-103">Record Search Query Format</span></span>

<span data-ttu-id="422e4-104">Un appel à la fonction [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) nécessite un paramètre de chaîne de requête XML utilisé pour déterminer les critères de base d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="422e4-104">A call to the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function requires an XML query string parameter that is used to determine the basic criteria of a search.</span></span> <span data-ttu-id="422e4-105">Utilisez le schéma suivant pour formuler une chaîne XML :</span><span class="sxs-lookup"><span data-stu-id="422e4-105">Use the following schema to formulate an XML string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">

  <xs:simpleType name="alphanumType">
     <xs:restriction base="xs:string">
        <xs:pattern value="\c+"/>
     </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="operatorType">
      <xs:choice maxOccurs="unbounded">
         <xs:element ref="and" />
         <xs:element ref="or" />
         <xs:element ref="clause" />
      </xs:choice>
  </xs:complexType>

  <xs:element name="and" type="operatorType"/>

  <xs:element name="or" type="operatorType"/>

  <xs:element name="clause">
      <xs:complexType>
          <xs:simpleContent>
              <xs:extension base="xs:string">
        <xs:attribute name="attrib" type="alphanumType" />
        <xs:attribute name="type">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="string"/>
                      <xs:enumeration value="date"/>
                      <xs:enumeration value="int"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
        <xs:attribute name="compare" default="equal">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="equal"/>
                      <xs:enumeration value="greater"/>
                      <xs:enumeration value="less"/>
                      <xs:enumeration value="notequal"/>
                      <xs:enumeration value="greaterorequal"/>
                      <xs:enumeration value="lessorequal"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:attribute>
              </xs:extension>
          </xs:simpleContent>
      </xs:complexType>
  </xs:element>

  <xs:element name="peersearch">
      <xs:complexType>
          <xs:choice>
              <xs:element ref="clause" />
              <xs:element ref="and" />
              <xs:element ref="or" />
          </xs:choice>
      </xs:complexType>
  </xs:element>
</xs:schema> 
```

### <a name="elements-to-use-for-a-record-search"></a><span data-ttu-id="422e4-106">Éléments à utiliser pour une recherche d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="422e4-106">Elements to Use for a Record Search</span></span>

<span data-ttu-id="422e4-107">L’élément principal d’une recherche d’enregistrements est **peersearch**, qui contient le Uniform Resource Identifier (Uri) du schéma associé dans l’attribut **xmlns** .</span><span class="sxs-lookup"><span data-stu-id="422e4-107">The primary element in a record search is **peersearch**, which contains the Uniform Resource Identifier (URI) of the associated schema in the **xmlns** attribute.</span></span> <span data-ttu-id="422e4-108">Quand **peersearch** est utilisé en tant qu’élément enfant, vous pouvez utiliser les **clauses** **and**, et **ou** en tant qu’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="422e4-108">When **peersearch** is used as a child element, you can use **and**, **clause**, and **or** as child elements.</span></span>

-   <span data-ttu-id="422e4-109">**et** -l’élément **et** effectue une opération and logique sur une ou plusieurs clauses contenues entre les balises d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="422e4-109">**and** - The **and** element performs a logical AND operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="422e4-110">Les **autres balises and et** **or** peuvent être des enfants, et les résultats récursifs de leurs clauses enfants sont inclus dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="422e4-110">Other **and** and **or** tags can be children, and recursive results of their child clauses are included in the operation.</span></span>

    <span data-ttu-id="422e4-111">Par exemple, si vous souhaitez obtenir un enregistrement qui contient un nom égal à James Peters et une dernière mise à jour supérieure à 2/28/2003, ou une date de création inférieure à 1/31/2003, utilisez la chaîne de requête XML suivante :</span><span class="sxs-lookup"><span data-stu-id="422e4-111">For example, if you want to obtain a record that contains a name equal to James Peters, and a last update that is greater than 2/28/2003, or a creation date that is less than 1/31/2003, use the following XML query string:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <and>
          <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
          <or>
             <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
             <clause attrib="peercreationtime" type="date" compare="less">2003-02-328</clause>
          </or>
       </and>
    </peersearch>
    ```

<!-- -->

-   <span data-ttu-id="422e4-112">**clause** : l’élément **clause** spécifie une règle comparative de base qui compare la valeur d’un attribut d’enregistrement spécifique à la valeur contenue entre les balises d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="422e4-112">**clause** - The **clause** element specifies a basic comparative rule that compares the value of a specific record attribute with the value contained between the opening and closing tags.</span></span> <span data-ttu-id="422e4-113">Les attributs **type** et **compare** doivent être fournis **compare** indique l’opération de comparaison à effectuer.</span><span class="sxs-lookup"><span data-stu-id="422e4-113">The **type** and **compare** attributes must be provided **compare** indicates the comparison operation to be performed.</span></span> <span data-ttu-id="422e4-114">Par exemple, une recherche simple qui indique que tous les enregistrements correspondants doivent avoir une valeur **peercreatorid** égale à James Peters apparaît dans la chaîne de requête XML comme suit :</span><span class="sxs-lookup"><span data-stu-id="422e4-114">For example, a simple search that indicates all matched records must have a **peercreatorid** value equal to James Peters appears in the XML query string as the following:</span></span>

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    <span data-ttu-id="422e4-115">Les attributs de **type** communs incluent **int**, **String** et **Date**.</span><span class="sxs-lookup"><span data-stu-id="422e4-115">Common **type** attributes include **int**, **string**, and **date**.</span></span> <span data-ttu-id="422e4-116">L’attribut **Date** peut être l’un des formats de date standard décrits dans [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="422e4-116">The **date** attribute can be one of the standard date formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>

    <span data-ttu-id="422e4-117">Les valeurs de l’attribut de **comparaison** sont **égales**, **NotEqual**, **inférieur**, **supérieur**, **lessorequal** et **greaterorequal**.</span><span class="sxs-lookup"><span data-stu-id="422e4-117">Values for the **compare** attribute are **equal**, **notequal**, **less**, **greater**, **lessorequal**, and **greaterorequal**.</span></span>

<!-- -->

-   <span data-ttu-id="422e4-118">**ou** -l’élément **ou** effectue une opération OR logique sur une ou plusieurs clauses contenues entre les balises d’ouverture et de fermeture.</span><span class="sxs-lookup"><span data-stu-id="422e4-118">**or** - The **or** element performs a logical OR operation on one or more clauses contained between the opening and closing tags.</span></span> <span data-ttu-id="422e4-119">D’autres éléments **ou** **et et peuvent** être des enfants, et les résultats récursifs des clauses enfants sont inclus dans l’opération.</span><span class="sxs-lookup"><span data-stu-id="422e4-119">Other **or** and **and** elements can be children, and recursive results of the child clauses are included in the operation.</span></span> <span data-ttu-id="422e4-120">Par exemple, si vous souhaitez obtenir un enregistrement qui contient un nom égal à James Peters, ou une dernière mise à jour comprise entre 1/31/2003 et 2/28/2003, utilisez la chaîne de requête XML suivante :</span><span class="sxs-lookup"><span data-stu-id="422e4-120">For example, if you want to obtain a record that contains a name equal to James Peters, or a last update that is between 1/31/2003 and 2/28/2003, use the following XML query string:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <or>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </or>
</peersearch>
```

## <a name="more-information-about-a-record-search"></a><span data-ttu-id="422e4-121">Plus d’informations sur la recherche d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="422e4-121">More Information About a Record Search</span></span>

<span data-ttu-id="422e4-122">Le premier niveau de nœuds après **peersearch** ne peut avoir qu’un seul élément.</span><span class="sxs-lookup"><span data-stu-id="422e4-122">The first level of nodes after **peersearch** can have only one element.</span></span> <span data-ttu-id="422e4-123">Toutefois, les enfants suivants de cet élément peuvent avoir de nombreux éléments au même niveau.</span><span class="sxs-lookup"><span data-stu-id="422e4-123">However, subsequent children of that element can have many elements at the same level.</span></span>

<span data-ttu-id="422e4-124">La requête de recherche suivante est incorrecte :</span><span class="sxs-lookup"><span data-stu-id="422e4-124">The following search query is incorrect:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
   <and>
      <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
      <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
   </and>
</peersearch>
```

<span data-ttu-id="422e4-125">La requête échoue parce que deux valeurs sont retournées pour la correspondance sans être résolues en une valeur true/false, ce qui signifie qu’une clause est une requête pour le nom d’un enregistrement qui est égal à James Peters, et que l’opération AND correspond aux deux clauses de composant.</span><span class="sxs-lookup"><span data-stu-id="422e4-125">The query fails because two values are returned for the match without being resolved into one true/false value, which means that one clause is a query for the name of a record that equals James Peters, and the AND operation matches the two component clauses.</span></span> <span data-ttu-id="422e4-126">Le résultat est deux valeurs logiques true/false qui sont contradictoires.</span><span class="sxs-lookup"><span data-stu-id="422e4-126">The result is two logical true/false values that are contradictory.</span></span>

<span data-ttu-id="422e4-127">Pour obtenir tous les enregistrements qui contiennent un nom égal à James Peters et une dernière mise à jour comprise entre 1/31/2003 et 2/28/2003, placez la **clause** **et les balises** et qui se trouvent au même niveau entre les balises d’ouverture et de fermeture **et** .</span><span class="sxs-lookup"><span data-stu-id="422e4-127">To obtain all records that contain a name equal to James Peters, and a last update that is between 1/31/2003 and 2/28/2003, place the **clause** and **and** tags that are at the same level between opening and closing **and** tags.</span></span> <span data-ttu-id="422e4-128">L’exemple suivant illustre la requête réussie :</span><span class="sxs-lookup"><span data-stu-id="422e4-128">The following example shows you the successful query:</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?> 
<peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
    <and>
      <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
      <and>
         <clause attrib="peerlastmodificationtime" type="date" compare="greater">2003-01-31</clause>
         <clause attrib="peerlastmodificationtime" type="date" compare="less">2003-02-28</clause>
      </and>
   </and>
</peersearch>
```

<span data-ttu-id="422e4-129">La liste suivante identifie d’autres informations spécifiques que vous devez connaître pour écrire une requête réussie :</span><span class="sxs-lookup"><span data-stu-id="422e4-129">The following list identifies other specific information that you must know to write a successful query:</span></span>

-   <span data-ttu-id="422e4-130">Les balises **et** et **ou** ne peuvent pas être situées entre les balises de **clause** d’ouverture et de fermeture, car, dans cette configuration, elles sont interprétées comme faisant partie de la valeur à laquelle il faut faire correspondre, ce qui génère une erreur ou une correspondance infructueuse.</span><span class="sxs-lookup"><span data-stu-id="422e4-130">The **and** and **or** tags cannot be located between opening and closing **clause** tags because, in that configuration, they are interpreted as part of the value to match against, which results in an error or a failed match.</span></span>
-   <span data-ttu-id="422e4-131">Chaque **paire de balises and et** **or** ouvrantes et fermantes doit inclure au moins un ou plusieurs nœuds enfants.</span><span class="sxs-lookup"><span data-stu-id="422e4-131">Each pair of **and** and **or** opening and closing tags must include at least one or more child nodes.</span></span>
-   <span data-ttu-id="422e4-132">Un jeu d’éléments zéro n’est pas autorisé dans ce schéma.</span><span class="sxs-lookup"><span data-stu-id="422e4-132">A zero set of elements is not allowed in this schema.</span></span>

## <a name="record-attributes"></a><span data-ttu-id="422e4-133">Attributs d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="422e4-133">Record Attributes</span></span>

<span data-ttu-id="422e4-134">En utilisant le [schéma d’attribut d’enregistrement](record-attribute-schema.md), un utilisateur peut créer des attributs d’enregistrement que l’attribut XML **Attrib** dans un élément de clause spécifie.</span><span class="sxs-lookup"><span data-stu-id="422e4-134">By using the [Record Attribute Schema](record-attribute-schema.md), a user can create record attributes that the **attrib** XML attribute in a clause element specifies.</span></span> <span data-ttu-id="422e4-135">Les attributs d’un nouvel enregistrement sont ajoutés en définissant le membre **pszAttributes** de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) sur une chaîne XML en utilisant le format spécifié dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="422e4-135">Attributes for a new record are added by setting the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) to an XML string using the format specified in the schema.</span></span>

<span data-ttu-id="422e4-136">L’infrastructure homologue réserve les noms d’attributs suivants :</span><span class="sxs-lookup"><span data-stu-id="422e4-136">The Peer Infrastructure reserves the following attribute names:</span></span>

-   <span data-ttu-id="422e4-137">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="422e4-137">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="422e4-138">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="422e4-138">**peercreatorid**</span></span>
-   <span data-ttu-id="422e4-139">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="422e4-139">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="422e4-140">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="422e4-140">**peerrecordid**</span></span>
-   <span data-ttu-id="422e4-141">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="422e4-141">**peerrecordtype**</span></span>
-   <span data-ttu-id="422e4-142">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="422e4-142">**peercreationtime**</span></span>
-   <span data-ttu-id="422e4-143">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="422e4-143">**peerlastmodificationtime**</span></span>

## <a name="special-characters"></a><span data-ttu-id="422e4-144">Caractères spéciaux</span><span class="sxs-lookup"><span data-stu-id="422e4-144">Special Characters</span></span>

<span data-ttu-id="422e4-145">Certains caractères peuvent être utilisés pour exprimer des modèles correspondants, ou pour échapper d’autres caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="422e4-145">Certain characters can be used to express matching patterns, or to escape other special characters.</span></span> <span data-ttu-id="422e4-146">Ces caractères sont décrits dans le tableau ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="422e4-146">These characters are described in the table below.</span></span> 

| <span data-ttu-id="422e4-147">Modèle de caractère</span><span class="sxs-lookup"><span data-stu-id="422e4-147">Character pattern</span></span> | <span data-ttu-id="422e4-148">Description</span><span class="sxs-lookup"><span data-stu-id="422e4-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | <span data-ttu-id="422e4-149">Caractère générique.</span><span class="sxs-lookup"><span data-stu-id="422e4-149">The wildcard character.</span></span> <span data-ttu-id="422e4-150">Lorsque ce caractère est rencontré dans une valeur de clause, il correspond à 0-n caractères de n’importe quelle valeur, y compris les espaces blancs et les caractères non alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="422e4-150">When this character is encountered in a clause value, it matches 0-n characters of any value, including whitespace and nonalphanumeric characters.</span></span> <span data-ttu-id="422e4-151">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="422e4-151">For example:</span></span><br/> <span data-ttu-id="422e4-152">«<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>»</span><span class="sxs-lookup"><span data-stu-id="422e4-152">"<clause attrib="peercreatorid" type="string" compare="equal">James P\*</clause>"</span></span><br/> <span data-ttu-id="422e4-153">Cette clause met en correspondance toutes les valeurs **peercreatorid** avec le prénom « James » et le nom de famille commençant par « P ».</span><span class="sxs-lookup"><span data-stu-id="422e4-153">This clause matches all **peercreatorid** values with a first name of "James" and a last name starting with "P".</span></span><br/> |
| \\\*              | <span data-ttu-id="422e4-154">Astérisque placé dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="422e4-154">An escaped asterisk.</span></span> <span data-ttu-id="422e4-155">Cette séquence correspond à un astérisque.</span><span class="sxs-lookup"><span data-stu-id="422e4-155">This sequence matches an asterisk character.</span></span>                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="422e4-156">?</span><span class="sxs-lookup"><span data-stu-id="422e4-156">?</span></span>                 | <span data-ttu-id="422e4-157">Caractère générique à un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="422e4-157">The single-character wildcard character.</span></span> <span data-ttu-id="422e4-158">Lorsque ce caractère est rencontré dans une valeur de clause, il correspond à n’importe quel caractère unique, y compris les espaces blancs et les caractères non alphanumériques. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="422e4-158">When this character is encountered in a clause value, it matches any single character, including whitespace and nonalphanumeric characters.For example:</span></span><br/> <span data-ttu-id="422e4-159">«<clause attrib="filename" type="string" compare="equal">données-0 ?. XML</clause>»</span><span class="sxs-lookup"><span data-stu-id="422e4-159">"<clause attrib="filename" type="string" compare="equal">data-0?.xml</clause>"</span></span><br/> <span data-ttu-id="422e4-160">Cette clause correspond aux valeurs de **nom de fichier** telles que « data-01.xml » et « data-0B.xml ».</span><span class="sxs-lookup"><span data-stu-id="422e4-160">This clause matches **filename** values like "data-01.xml" and "data-0B.xml".</span></span><br/>                              |
| <span data-ttu-id="422e4-161">\\?</span><span class="sxs-lookup"><span data-stu-id="422e4-161">\\?</span></span>               | <span data-ttu-id="422e4-162">Point d’interrogation placé dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="422e4-162">An escaped question mark.</span></span> <span data-ttu-id="422e4-163">Cette séquence correspond à un caractère point d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="422e4-163">This sequence matches a question mark character.</span></span>                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | <span data-ttu-id="422e4-164">Barre oblique inverse placée dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="422e4-164">An escaped backslash.</span></span> <span data-ttu-id="422e4-165">Cette séquence correspond à une barre oblique inverse unique.</span><span class="sxs-lookup"><span data-stu-id="422e4-165">This sequence matches a single backslash character.</span></span>                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="422e4-166">Si la séquence de caractères n’est pas valide, la fonction [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) retourne l’erreur **E \_ INVALIDARG**.</span><span class="sxs-lookup"><span data-stu-id="422e4-166">If the character sequence is not valid, the [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) function returns the error **E\_INVALIDARG**.</span></span> <span data-ttu-id="422e4-167">Une séquence non valide est une séquence qui contient un \\ caractère « » (barre oblique inverse) qui n’est pas immédiatement suivi d’un \* caractère « » (astérisque), d’un «  ? » (point d’interrogation), ou un autre \\ caractère «» (barre oblique inverse).</span><span class="sxs-lookup"><span data-stu-id="422e4-167">An invalid sequence is any sequence that contains a "\\" (backslash) character not immediately followed by either an "\*" (asterisk) character, a "?" (question mark) character, or another "\\" (backslash) character.</span></span>

 

 




