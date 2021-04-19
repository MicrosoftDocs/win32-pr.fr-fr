---
description: Utilisation d’un ordinateur par révolution HTTP en permettant aux utilisateurs d’utiliser un navigateur Web pour accéder facilement aux informations sur un serveur distant sur un réseau.
ms.assetid: 44f3ff21-4978-4902-aa74-ddeef60881db
title: Vue d’ensemble du service SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b93ce7d80753f306777d3ac0b77dc46dc4e08d22
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514932"
---
# <a name="com-soap-service-overview"></a>Vue d’ensemble du service SOAP COM+

Utilisation d’un ordinateur par révolution HTTP en permettant aux utilisateurs d’utiliser un navigateur Web pour accéder facilement aux informations sur un serveur distant sur un réseau. Les services Web XML ont à présent révolutionné le développement d’applications en permettant aux applications clientes d’appeler facilement des méthodes à distance sur un réseau.

Il est souvent utile pour une application cliente de pouvoir appeler une méthode implémentée sur un serveur distant. Parfois, la méthode utilise des informations volatiles stockées sur le serveur distant (par exemple, une méthode qui retourne le prix actuel du stock correspondant à un symbole de titre donné). À d’autres moments, le développeur souhaite pouvoir mettre à niveau l’implémentation des méthodes sans avoir à redéployer toutes les applications qui l’utilisent.

Comme les pages Web, les services Web XML sont accessibles via un serveur Web, par exemple IIS, à l’aide de HTTP. Toutefois, au lieu des pages Web encodées en HTML, ces paquets HTTP contiennent les paramètres d’entrée et de sortie des appels à une méthode implémentée sur le serveur, encodé dans SOAP.

Pour utiliser un service Web XML, vous devez connaître l’URL où le service est exposé et le nom de la méthode que vous souhaitez appeler, et vous devez fournir les paramètres d’entrée à la méthode. [La norme SOAP 1,1](https://www.w3.org/TR/SOAP/) fournit l’exemple suivant d’un paquet http contenant un appel distant à un service Web XML à https://www.stockquoteserver.com/StockQuote , qui retourne le prix actuel du stock correspondant à un symbole de titre donné.

``` syntax
POST /StockQuote HTTP/1.1
Host: www.stockquoteserver.com
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn
SOAPAction: "Some-URI"

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding/">
<SOAP-ENV:Body>
<m:GetLastTradePrice xmlns:m="Some-URI">
<symbol>DIS</symbol>
</m:GetLastTradePrice>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Comme l’illustre l’exemple précédent, SOAP est une instance XML qui peut être incorporée dans une requête HTTP. De même, le résultat est retourné sous la forme d’un paquet HTTP avec une charge utile SOAP, comme indiqué dans l’exemple suivant.

``` syntax
HTTP/1.1 200 OK
Content-Type: text/xml; "charset=utf-8"
Content-Length: nnnn

<SOAP-ENV:Envelope
xmlns:SOAP-ENV="https://schemas.xmlsoap.org/soap/envelope/"
SOAP-ENV:encodingStyle="https://schemas.xmlsoap.org/soap/encoding//">
<SOAP-ENV:Body>
<m:GetLastTradePriceResponse xmlns:m="Some-URI">
<Price>34.5</Price>
</m:GetLastTradePriceResponse>
</SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

Bien qu’il soit utile d’avoir une compréhension de l’infrastructure sous-jacente aux services Web XML, COM+ facilite la création et l’utilisation de services Web XML que vous n’aurez pas souvent à plonger à ce niveau.

Vous pouvez exposer les méthodes dans les interfaces par défaut des composants COM configurés dans n’importe quelle application COM+ en tant que service Web XML. Aucune considération particulière de programmation n’est nécessaire lors de l’écriture des composants, sauf que les méthodes que vous souhaitez exposer doivent se trouver dans l’interface par défaut et que le composant doit être configuré (dans le catalogue COM+ de votre serveur). Vous n’avez pas besoin d’écrire du code pour communiquer via une interface réseau ou pour analyser le protocole SOAP. Pour obtenir des instructions détaillées sur l’utilisation du service SOAP COM+ pour créer un service Web XML, consultez [création de services Web XML](creating-xml-web-services.md).

Lorsque vous exposez une application COM+ en tant que service Web XML, des informations détaillées sur la syntaxe de toutes les méthodes disponibles à partir d’un service Web XML sont publiées automatiquement, à l’aide de l’Web Services Description Language (WSDL). Ces informations sont utilisées par les clients qui utilisent votre service Web XML.

COM+ vous offre deux moyens d’accéder à un service Web XML distant et de l’utiliser, comme suit :

-   Le mode WKO ( *bien connu* ) peut être utilisé pour accéder à n’importe quel service Web XML qui publie sa syntaxe à l’aide de WSDL, même si ce service Web XML n’a pas été créé à l’aide de com+ ou même de Microsoft Windows.
-   Le mode de l' *objet activé* par le client (CAO) peut être utilisé uniquement pour accéder aux services Web XML créés en exposant des applications com+. Le mode CAO augmente les performances en utilisant des connexions persistantes, une fonctionnalité qui n’est pas prise en charge par la norme SOAP actuelle.

Ces deux méthodes permettent aux applications clientes d’appeler des méthodes de services Web XML à distance de manière simple, sans avoir à écrire du code pour communiquer via une interface réseau ou pour analyser SOAP. Pour plus d’informations sur l’accès aux services Web XML dans les deux modes, consultez [accès aux services Web XML en mode CAO](accessing-xml-web-services-in-cao-mode.md) et [accès aux services Web XML en mode WKO](accessing-xml-web-services-in-wko-mode.md).

> [!Note]  
> COM+ ne prend en charge que la spécification SOAP-RPC, et non la spécification SOAP-Document.

 

COM+ facilite grandement l’utilisation des services Web XML en vous permettant d’utiliser des applications COM+ existantes en tant que services Web XML en mode CAO de manière totalement transparente. Si vous [exportez](exporting-a-soap-enabled-application.md) une application com+ qui a été exposée en tant que service Web XML à partir de votre serveur, tout client qui [importe](importing-a-soap-enabled-application.md) l’application peut utiliser de manière transparente le service Web XML du serveur chaque fois que l’application importée est utilisée. Cette fonctionnalité permet de convertir très facilement les applications COM+ existantes en services Web XML et le déploiement de ces services sur un réseau.

L’utilisation des services Web XML présente plusieurs avantages par rapport aux autres implémentations des appels de procédure distante (RPC), y compris les éléments suivants :

-   SOAP est une véritable implémentation de RPC multiplateforme qui augmente l’interopérabilité.
-   Les services Web XML prennent en charge les méthodes avec les paramètres d’entrée et de sortie.
-   Les services Web XML s’exécutent sur HTTP, ce qui peut généralement pénétrer les pare-feu susceptibles de bloquer d’autres implémentations RPC.
-   Lorsqu’un service Web XML est implémenté à l’aide de COM+, le développeur n’a pas à écrire de code spécialisé. Il s’agit d’un énorme avantage par rapport aux autres mécanismes RPC.

> [!Note]  
> Les services Web XML ne prennent pas en charge les appels transactionnels asynchrones ou en toute transparence. Utilisez le service [composants en file d’attente com+](com--queued-components.md) lorsque vous avez besoin de cette fonctionnalité.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur la sécurité du service SOAP COM+](com--soap-service-security-considerations.md)
</dt> </dl>

 

 



