---
title: IAgentCharacter afficher
description: IAgentCharacter afficher
ms.assetid: 5f13dcef-3777-41eb-827f-6162bad71a2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 997a9879d564644085bd92e4515460c3dde33208
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031243"
---
# <a name="iagentcharactershow"></a>IAgentCharacter :: Show

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Show(
   long bFast,      // play Showing state animation flag
   long * pdwReqID  // address of request ID
);
```

Affiche un caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, *pdwReqID* contient l’ID de la demande.

<dl> <dt>

<span id="bFast"></span><span id="bfast"></span><span id="BFAST"></span>*bFast*
</dt> <dd>

Indication de l’indicateur d’animation d’État. Si ce paramètre a la **valeur true**, l’animation de l’état d' **affichage** est lue après que le caractère a été visible ; Si la **valeur est false**, l’animation n’est pas lue.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de demande [**Show**](/windows/desktop/lwef/iagentcharacter--show) .

</dd> </dl>

Évitez d’affecter la **valeur true** au paramètre *bFast* sans avoir à utiliser une animation au préalable ; sinon, le frame de caractères peut être affiché, mais n’a aucune image à afficher. En particulier, Notez que si vous appelez [**MoveTo**](iagentcharacter--moveto.md) alors que le caractère n’est pas visible, aucune animation n’est lue. Par conséquent, si vous appelez la méthode **Show** avec *BFast* défini sur **true**, aucune image ne sera affichée. De même, si vous appelez [**Hide**](/windows/desktop/lwef/iagentcharacter--hide)et **Show** avec *bFast* défini sur **true**, il n’y aura aucune image visible.

Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité de l’animation de l’état d' **émission** avant d’appeler cette méthode.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: Hide**](iagentcharacter--hide.md)


 

 