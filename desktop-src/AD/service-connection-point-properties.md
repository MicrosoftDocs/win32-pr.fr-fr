---
title: Propriétés du point de connexion de service
description: Les attributs de la classe serviceConnectionPoint sont suffisants pour la plupart des services.
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- Propriétés du point de connexion de service
- points de connexion de service AD, propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101424"
---
# <a name="service-connection-point-properties"></a>Propriétés du point de connexion de service

Les attributs de la classe **serviceConnectionPoint** sont suffisants pour la plupart des services. Active Directory Domain Services ne définissent pas la manière dont les attributs sont utilisés, les clients de votre service doivent être en mesure d’interpréter et d’utiliser les données de votre service SCP. Les services qui doivent publier des données supplémentaires sur elles-mêmes peuvent étendre le schéma Active Directory en créant une sous-classe de la classe **serviceConnectionPoint** , donnant à la sous-classe un nom distinct. Pour plus d’informations sur les extensions de schéma, consultez [extension du schéma](extending-the-schema.md).

Les attributs les plus importants d’un SCP sont les **Mots clés**, **servicednsname**, **serviceDNSNameType**, **serviceClassName** et **serviceBindingInformation**. Les applications clientes recherchent dans le répertoire des valeurs de **Mots clés** pour localiser votre SCP. Lorsque votre SCP est trouvé, les clients peuvent lire d’autres attributs pour récupérer les données du service.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>mot</strong><br/></td>
<td>L’attribut <strong>Keywords</strong> peut contenir plusieurs valeurs de chaîne qui identifient votre service. Cet attribut est inclus dans le catalogue global, ce qui signifie que les clients d’un domaine d’une forêt d’entreprise peuvent rechercher les mots clés associés à votre service dans le catalogue global. Cet attribut est également indexé, ce qui améliore les performances des requêtes. Le programme d’installation qui crée le SCP définit les valeurs de l’attribut <strong>Keywords</strong> . En règle générale, ces valeurs ne sont pas modifiées par le service actif.<br/> Les mots clés exacts que vous devez inclure dans votre SCP dépendent de la façon dont les clients recherchent votre service. Les mots clés les plus utilisés sont les chaînes GUID parce que les GUID sont garantis comme uniques dans une forêt. Utilisez le format de chaîne GUID renvoyé par la fonction <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> dans la bibliothèque RPC. Vous pouvez également inclure des noms explicites, si les clients peuvent les utiliser pour rechercher votre service. Les mots clés dans un SCP doivent inclure des chaînes GUID et/ou des noms qui identifient les données suivantes sur votre service :
<ul>
<li>Votre entreprise ou organisation : par exemple, fabrikam.</li>
<li>Le produit ou service : par exemple, SQL Server. Cela permet aux applications clientes de trouver des SCP pour les services de ce type.</li>
<li>Version spécifique du produit ou service, par exemple 7,5.</li>
<li>Pour les SCP qui publient un ensemble spécifique de données ou de fonctionnalités pour un type de service, incluez une chaîne GUID ou un nom qui identifie l’instance spécifique. Par exemple, un service de base de données peut publier un SCP pour une base de données spécifique. Dans ce cas, le SCP inclut un GUID de produit pour identifier le service et un autre GUID pour identifier la base de données.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>servicednsname</strong> et <strong>serviceDNSNameType</strong><br/></td>
<td>Les applications clientes utilisent les attributs <strong>servicednsname</strong> et <strong>serviceDNSNameType</strong> pour déterminer l’ordinateur hôte du service. La valeur <strong>serviceDNSNameType</strong> indique le type de nom DNS spécifié par <strong>ServiceDNSName</strong> généralement &quot; &quot; si <strong>servicednsname</strong> contient un nom d’hôte ou &quot; SRV &quot; si <strong>servicednsname</strong> contient un nom d’enregistrement SRV.<br/> La valeur <strong>servicednsname</strong> est généralement le nom DNS de l’ordinateur hôte du service. Votre programme d’installation de service peut appeler la fonction <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> pour récupérer le nom DNS de l’ordinateur local.<br/> Pour les services qui ont des enregistrements SRV DNS, <strong>servicednsname</strong> peut être le nom de l’enregistrement SRV. Une application cliente utilise les API DNS pour récupérer tous les enregistrements SRV qui correspondent à ce nom. Le client récupère ensuite le nom d’hôte DNS à partir de l’un des enregistrements SRV. Cette technique est utile pour les services répliqués, car les enregistrements SRV incluent également des données qui permettent au client de sélectionner le meilleur réplica.<br/></td>
</tr>
<tr class="odd">
<td><strong>serviceBindingInformation</strong><br/></td>
<td>Propriété à valeurs multiples qui contient des valeurs de chaîne qui stockent les données requises pour la liaison à un service. Cette propriété est indexée et est répliquée dans le catalogue global.<br/> Le contenu de <strong>serviceBindingInformation</strong> est spécifique au service qui a publié le SCP ; les clients doivent interpréter les données de liaison. Dans le cas le plus courant, les données de liaison se composent d’un numéro de port sur l’ordinateur hôte du service.<br/></td>
</tr>
<tr class="even">
<td><strong>serviceClassName</strong><br/></td>
<td>Propriété à valeur unique qui identifie la classe de service représentée par le SCP. Il s’agit d’une chaîne descriptive spécifique au service qui a publié le SCP. par exemple, SqlServer. Pour les services qui prennent en charge l’authentification mutuelle, les clients peuvent utiliser cette propriété, ainsi que le nom DNS de l’ordinateur hôte du service, pour former un nom de principal du service. Pour plus d’informations, consultez <a href="mutual-authentication-using-kerberos.md">authentification mutuelle à l’aide de Kerberos</a>.<br/></td>
</tr>
</tbody>
</table>



 

 

