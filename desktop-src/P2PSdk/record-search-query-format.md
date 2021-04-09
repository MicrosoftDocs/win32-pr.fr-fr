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
# <a name="record-search-query-format"></a>Format de requête de recherche d’enregistrements

Un appel à la fonction [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) nécessite un paramètre de chaîne de requête XML utilisé pour déterminer les critères de base d’une recherche. Utilisez le schéma suivant pour formuler une chaîne XML :

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

### <a name="elements-to-use-for-a-record-search"></a>Éléments à utiliser pour une recherche d’enregistrements

L’élément principal d’une recherche d’enregistrements est **peersearch**, qui contient le Uniform Resource Identifier (Uri) du schéma associé dans l’attribut **xmlns** . Quand **peersearch** est utilisé en tant qu’élément enfant, vous pouvez utiliser les **clauses** **and**, et **ou** en tant qu’éléments enfants.

-   **et** -l’élément **et** effectue une opération and logique sur une ou plusieurs clauses contenues entre les balises d’ouverture et de fermeture. Les **autres balises and et** **or** peuvent être des enfants, et les résultats récursifs de leurs clauses enfants sont inclus dans l’opération.

    Par exemple, si vous souhaitez obtenir un enregistrement qui contient un nom égal à James Peters et une dernière mise à jour supérieure à 2/28/2003, ou une date de création inférieure à 1/31/2003, utilisez la chaîne de requête XML suivante :

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

-   **clause** : l’élément **clause** spécifie une règle comparative de base qui compare la valeur d’un attribut d’enregistrement spécifique à la valeur contenue entre les balises d’ouverture et de fermeture. Les attributs **type** et **compare** doivent être fournis **compare** indique l’opération de comparaison à effectuer. Par exemple, une recherche simple qui indique que tous les enregistrements correspondants doivent avoir une valeur **peercreatorid** égale à James Peters apparaît dans la chaîne de requête XML comme suit :

    ``` syntax
    <?xml version="1.0" encoding="utf-8" ?> 
    <peersearch xmlns:xs="https://www.w3.org/2001/XMLSchema">
       <clause attrib="peercreatorid" type="string" compare="equal">James Peters</clause>
    </peersearch>
    ```

    Les attributs de **type** communs incluent **int**, **String** et **Date**. L’attribut **Date** peut être l’un des formats de date standard décrits dans [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .

    Les valeurs de l’attribut de **comparaison** sont **égales**, **NotEqual**, **inférieur**, **supérieur**, **lessorequal** et **greaterorequal**.

<!-- -->

-   **ou** -l’élément **ou** effectue une opération OR logique sur une ou plusieurs clauses contenues entre les balises d’ouverture et de fermeture. D’autres éléments **ou** **et et peuvent** être des enfants, et les résultats récursifs des clauses enfants sont inclus dans l’opération. Par exemple, si vous souhaitez obtenir un enregistrement qui contient un nom égal à James Peters, ou une dernière mise à jour comprise entre 1/31/2003 et 2/28/2003, utilisez la chaîne de requête XML suivante :

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

## <a name="more-information-about-a-record-search"></a>Plus d’informations sur la recherche d’enregistrements

Le premier niveau de nœuds après **peersearch** ne peut avoir qu’un seul élément. Toutefois, les enfants suivants de cet élément peuvent avoir de nombreux éléments au même niveau.

La requête de recherche suivante est incorrecte :

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

La requête échoue parce que deux valeurs sont retournées pour la correspondance sans être résolues en une valeur true/false, ce qui signifie qu’une clause est une requête pour le nom d’un enregistrement qui est égal à James Peters, et que l’opération AND correspond aux deux clauses de composant. Le résultat est deux valeurs logiques true/false qui sont contradictoires.

Pour obtenir tous les enregistrements qui contiennent un nom égal à James Peters et une dernière mise à jour comprise entre 1/31/2003 et 2/28/2003, placez la **clause** **et les balises** et qui se trouvent au même niveau entre les balises d’ouverture et de fermeture **et** . L’exemple suivant illustre la requête réussie :

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

La liste suivante identifie d’autres informations spécifiques que vous devez connaître pour écrire une requête réussie :

-   Les balises **et** et **ou** ne peuvent pas être situées entre les balises de **clause** d’ouverture et de fermeture, car, dans cette configuration, elles sont interprétées comme faisant partie de la valeur à laquelle il faut faire correspondre, ce qui génère une erreur ou une correspondance infructueuse.
-   Chaque **paire de balises and et** **or** ouvrantes et fermantes doit inclure au moins un ou plusieurs nœuds enfants.
-   Un jeu d’éléments zéro n’est pas autorisé dans ce schéma.

## <a name="record-attributes"></a>Attributs d’enregistrement

En utilisant le [schéma d’attribut d’enregistrement](record-attribute-schema.md), un utilisateur peut créer des attributs d’enregistrement que l’attribut XML **Attrib** dans un élément de clause spécifie. Les attributs d’un nouvel enregistrement sont ajoutés en définissant le membre **pszAttributes** de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) sur une chaîne XML en utilisant le format spécifié dans le schéma.

L’infrastructure homologue réserve les noms d’attributs suivants :

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="special-characters"></a>Caractères spéciaux

Certains caractères peuvent être utilisés pour exprimer des modèles correspondants, ou pour échapper d’autres caractères spéciaux. Ces caractères sont décrits dans le tableau ci-dessous. 

| Modèle de caractère | Description                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*                | Caractère générique. Lorsque ce caractère est rencontré dans une valeur de clause, il correspond à 0-n caractères de n’importe quelle valeur, y compris les espaces blancs et les caractères non alphanumériques. Par exemple :<br/> «<clause attrib="peercreatorid" type="string" compare="equal">James P \* </clause>»<br/> Cette clause met en correspondance toutes les valeurs **peercreatorid** avec le prénom « James » et le nom de famille commençant par « P ».<br/> |
| \\\*              | Astérisque placé dans une séquence d’échappement. Cette séquence correspond à un astérisque.                                                                                                                                                                                                                                                                                                                                                                       |
| ?                 | Caractère générique à un seul caractère. Lorsque ce caractère est rencontré dans une valeur de clause, il correspond à n’importe quel caractère unique, y compris les espaces blancs et les caractères non alphanumériques. Par exemple :<br/> «<clause attrib="filename" type="string" compare="equal">données-0 ?. XML</clause>»<br/> Cette clause correspond aux valeurs de **nom de fichier** telles que « data-01.xml » et « data-0B.xml ».<br/>                              |
| \\?               | Point d’interrogation placé dans une séquence d’échappement. Cette séquence correspond à un caractère point d’interrogation.                                                                                                                                                                                                                                                                                                                                                              |
| \\\\              | Barre oblique inverse placée dans une séquence d’échappement. Cette séquence correspond à une barre oblique inverse unique.                                                                                                                                                                                                                                                                                                                                                               |



 

Si la séquence de caractères n’est pas valide, la fonction [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords) retourne l’erreur **E \_ INVALIDARG**. Une séquence non valide est une séquence qui contient un \\ caractère « » (barre oblique inverse) qui n’est pas immédiatement suivi d’un \* caractère « » (astérisque), d’un «  ? » (point d’interrogation), ou un autre \\ caractère «» (barre oblique inverse).

 

 




