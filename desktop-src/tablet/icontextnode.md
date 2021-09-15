---
description: Représente un nœud dans une arborescence d’objets qui sont créés dans le cadre de l’analyse de l’encre.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interface IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525332"
---
# <a name="icontextnode-interface"></a>Interface IContextNode

Représente un nœud dans une arborescence d’objets qui sont créés dans le cadre de l’analyse de l’encre.

## <a name="members"></a>Membres

L’interface **IContextNode** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IContextNode** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IContextNode** possède ces méthodes.



| Méthode                                                                                  | Description                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddContextLink**](icontextnode-addcontextlink.md)                                   | Ajoute un nouveau [**IContextLink**](icontextlink.md) à la collection de liens de contexte de l’objet **IContextNode** .<br/>                                                                                                          |
| [**AddPropertyData**](icontextnode-addpropertydata.md)                                 | Ajoute un élément de données spécifiques à l’application.<br/>                                                                                                                                                                         |
| [**Répond**](icontextnode-confirm.md)                                                 | Modifie le type de confirmation, qui contrôle ce que l’objet [**IInkAnalyzer**](iinkanalyzer.md) peut modifier à propos du **IContextNode**.<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | Détermine si l’objet **IContextNode** contient des données stockées sous l’identificateur spécifié.<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | Crée un objet **IContextNode** enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | Crée un nouvel objet **IContextNode** enfant.<br/>                                                                                                                                                                       |
| [**DeleteContextLink**](icontextnode-deletecontextlink.md)                             | Supprime un objet [**IContextLink**](icontextlink.md) de la collection de liens de l’objet **IContextNode** .<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | Supprime un **IContextNode** enfant.<br/>                                                                                                                                                                                  |
| [**GetContextLinks**](icontextnode-getcontextlinks.md)                                 | Récupère une collection d’objets [**IContextLink**](icontextlink.md) qui représentent des relations avec d’autres objets **IContextNode** .<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | Récupère l’identificateur pour l’objet **IContextNode** .<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | Récupère la position et la taille de l’objet **IContextNode** .<br/>                                                                                                                                                    |
| [**GetParentNode**](icontextnode-getparentnode.md)                                     | Récupère le nœud parent de ce **IContextNode** dans l’arborescence du nœud de contexte.<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | Récupère la valeur qui indique si un objet **IContextNode** est partiellement rempli ou entièrement rempli.<br/>                                                                                                   |
| [**GetPropertyData**](icontextnode-getpropertydata.md)                                 | Récupère des données spécifiques à l’application ou d’autres données de propriété en fonction de l’identificateur spécifié.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Récupère les identificateurs pour lesquels il existe des données de propriété.<br/>                                                                                                                                                        |
| [**GetStrokeCount**](icontextnode-getstrokecount.md)                                   | Récupère le nombre de traits associés à l’objet **IContextNode** .<br/>                                                                                                                                       |
| [**GetStrokeId**](icontextnode-getstrokeid.md)                                         | Récupère l’identificateur de trait pour le trait référencé par une valeur d’index dans l’objet **IContextNode** .<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Récupère un tableau d’identificateurs pour les traits dans l’objet **IContextNode** .<br/>                                                                                                                              |
| [**GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.<br/>                                                                                                                                   |
| [**GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | Récupère les nœuds enfants directs de l’objet **IContextNode** .<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | Récupère le type de l’objet **IContextNode** .<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | Récupère un nom de type explicite de ce **IContextNode**.<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | Récupère une valeur qui indique si l’objet **IContextNode** est confirmé. [**IInkAnalyzer**](iinkanalyzer.md) ne peut pas modifier le type de nœud et les traits associés pour les objets **IContextNode** confirmés.<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | Recrée les données de propriété internes et spécifiques à l’application pour un tableau d’octets précédemment créé avec [**IContextNode :: SavePropertiesData**](icontextnode-savepropertiesdata.md).<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | Réorganise un objet **IContextNode** enfant spécifié à l’index spécifié.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Supprime une partie des données spécifiques à l’application.<br/>                                                                                                                                                                      |
| [**Apparenter**](icontextnode-reparent.md)                                               | Déplace cet objet **IContextNode** de la collection de sous-nœuds du nœud de contexte parent vers la collection de sous-nœuds du nœud de contexte spécifié.<br/>                                                                         |
| [**ReparentStrokeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | Déplace les données de trait de ce **IContextNode** vers le **IContextNode** spécifié.<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce **IContextNode**.<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Met à jour la position et la taille de ce **IContextNode**.<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | Modifie la valeur qui indique si ce **IContextNode** est partiellement ou entièrement rempli.<br/>                                                                                                                   |
| [**SetStrokes**](icontextnode-setstrokes.md)                                           | Associe les traits spécifiés à ce **IContextNode**.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Notes

Les types de nœuds sont décrits dans les constantes de [type de nœud de contexte](context-node-types.md) .

## <a name="examples"></a>Exemples

L’exemple suivant montre une méthode qui examine un **IContextNode**; la méthode effectue les opérations suivantes :

-   Obtient le type du nœud de contexte. Si le nœud de contexte est une encre non classifiée, un indicateur d’analyse ou un nœud de reconnaissance personnalisé, il appelle une méthode d’assistance pour examiner des propriétés spécifiques du type de nœud.
-   Si le nœud possède des sous-nœuds, il examine chaque sous-nœud en s’appelant lui-même.
-   Si le nœud est un nœud feuille manuscrit, il examine les données de trait du nœud en appelant une méthode d’assistance.

L’API position InkAnalysis vous permet de créer un nœud de ligne qui contient des mots et des mots de texte. Toutefois, l’analyseur ignore ces nœuds mixtes et les traite comme des nœuds étrangers. Cela aura un impact sur l’exactitude de l’analyse de la détection des annotations manuscrites lorsque l’utilisateur final écrit sur ce nœud mixte.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Types de nœuds de contexte](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

