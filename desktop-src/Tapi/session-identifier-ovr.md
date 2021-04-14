---
description: L’interface TAPI assigne des identificateurs de session qui sont uniques pour chaque session et application.
ms.assetid: 711a9bc6-ffc6-499b-8653-ba230028c146
title: Identificateur de session
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e135beb439d1c5fb2fdd46d4986cd35dc5ae49b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393803"
---
# <a name="session-identifier"></a>Identificateur de session

L’interface TAPI assigne des identificateurs de session qui sont uniques pour chaque session et application. Une application utilise un identificateur de session pour communiquer avec l’interface TAPI concernant une session spécifique. Une application obtient généralement un identificateur en créant une session de communication ou lorsque l’interface TAPI offre une session.

Un identificateur de session ne peut pas être utilisé pour transmettre des informations à une autre application. À cet effet, utilisez l' [ID d’appel](call-id-ovr.md), qui peut être assigné par un fournisseur de services.

Consultez [lancer une session](initiate-a-session-ovr.md) pour plus d’informations sur les opérations qui créent des sessions et retournent un identificateur de session. Consultez [répondre à la session lancée ailleurs](respond-to-session-initiated-elsewhere-ovr.md) pour les opérations qui acquièrent des identificateurs de session à partir de TAPI. Pour plus d’informations sur la libération des ressources de session, consultez [terminer une session](terminate-a-session-ovr.md) .

Tous les fournisseurs de services doivent prendre en charge une certaine forme d’identification de session.

**TAPI 2. x :** L’identificateur principal d’une session de communication est le descripteur d’appel.

**TAPI 3. x :** Une session est représentée par un [objet d’appel](call-object.md) et l’identificateur principal est un pointeur vers l’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

 

 



