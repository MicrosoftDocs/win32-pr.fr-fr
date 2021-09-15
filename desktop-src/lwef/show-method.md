---
title: Show, méthode
description: Show, méthode
ms.assetid: 58adbb55-f4cb-4356-abc4-b85fa3af744d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05a1adaa46c85f34e02128960330c68d9a86db1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413073"
---
# <a name="show-method"></a>Show, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Rend le caractère spécifié visible et lit l’animation **qui lui** est associée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Afficher_ *  \[ *rapidement*\]



| Partie   | Description                                                                                                                                                                                                                              |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Rapide* | facultatif. Expression booléenne spécifiant si le serveur lit l’animation d' **affichage** . **True** Ignore l’animation de l’état d' **émission** . <br/> **False** (valeur par défaut) n’ignore pas l’animation de l’état d' **émission** . <br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si **l’animation associée** n’a pas été chargée et que vous n’avez pas spécifié le paramètre **Fast** comme **true**, le serveur définit la propriété [**Status**](status-property.md) de l’objet **Request** sur « failed » avec un numéro d’erreur approprié. Par conséquent, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger l’animation de l’état d' **affichage** avant d’appeler la méthode **Show** .

Évitez d’affecter la **valeur true** au paramètre **Fast** sans avoir préalablement lu une animation. dans le cas contraire, le frame de caractère peut s’afficher sans image. En particulier, Notez que si vous appelez [**MoveTo**](moveto-method.md) alors que le caractère n’est pas visible, aucune animation n’est lue. Par conséquent, si vous appelez la méthode **Show** avec **fastd** défini sur **true**, aucune image ne s’affiche. De même, si vous appelez la fonction [**Hide**](hide-method.md) puis **Show** avec **Fast** Set à **true**, aucune image n’est visible.

## <a name="see-also"></a>Voir aussi

[**Hide (méthode)**](hide-method.md)


 

