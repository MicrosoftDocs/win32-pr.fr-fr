---
description: TSPIMessage est un type d’énumération qui définit l’ensemble des fonctions LINEEVENT et PHONEEVENT supplémentaires qui apparaissent dans TSPI qui n’apparaissent pas dans l’interface TAPI.
ms.assetid: b3c4ce68-033f-42f1-8c37-66326d21bf32
title: TSPIMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75ed5f081c367c675c565f64146b2201890b8306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753717"
---
# <a name="tspimessage"></a>TSPIMessage

**TSPIMessage** est un type d’énumération qui définit l’ensemble des fonctions [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) et [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) supplémentaires qui apparaissent dans TSPI qui n’apparaissent pas dans l’interface TAPI.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="TSPI_MESSAGE_BASE"></span><span id="tspi_message_base"></span>\_base de messages TSPI \_
</dt> <dd>

Nombre le plus bas dans la plage de valeurs de message spécifiques à TSPI. Cette valeur n’a aucune signification, mais sert de base pour définir les autres valeurs.

</dd> <dt>

<span id="LINE_NEWCALL"></span><span id="line_newcall"></span>NEWCALL de ligne \_
</dt> <dd>

Spécifie qu’un nouvel appel entrant est arrivé et l’introduit dans l’interface TAPI. Il doit s’agir du premier message envoyé à l’interface TAPI pour un nouvel appel entrant. L’interface TAPI retourne son identificateur opaque pour l’appel dans le cadre de sa gestion de ce message.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFIC"></span><span id="line_calldevspecific"></span>CALLDEVSPECIFIC de ligne \_
</dt> <dd>

Spécifie qu’un événement spécifique à l’appareil s’est produit sur un appareil d’appel.

</dd> <dt>

<span id="LINE_CALLDEVSPECIFICFEATURE"></span><span id="line_calldevspecificfeature"></span>CALLDEVSPECIFICFEATURE de ligne \_
</dt> <dd>

Spécifie qu’un événement de fonctionnalité spécifique à l’appareil s’est produit sur un appareil d’appel.

</dd> </dl>

 

 
