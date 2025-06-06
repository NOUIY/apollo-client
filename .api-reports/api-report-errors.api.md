## API Report File for "@apollo/client"

> Do not edit this file. It is a report generated by [API Extractor](https://api-extractor.com/).

```ts

import type { GraphQLError } from 'graphql';
import type { GraphQLErrorExtensions } from 'graphql';
import type { GraphQLFormattedError } from 'graphql';

// @public (undocumented)
export class ApolloError extends Error {
    constructor({ graphQLErrors, protocolErrors, clientErrors, networkError, errorMessage, extraInfo, }: ApolloErrorOptions);
    cause: ({
        readonly message: string;
        extensions?: GraphQLErrorExtensions[] | GraphQLFormattedError["extensions"];
    } & Omit<Partial<Error> & Partial<GraphQLFormattedError>, "extensions">) | null;
    // (undocumented)
    clientErrors: ReadonlyArray<Error>;
    // (undocumented)
    extraInfo: any;
    // (undocumented)
    graphQLErrors: ReadonlyArray<GraphQLFormattedError>;
    // (undocumented)
    message: string;
    // (undocumented)
    name: string;
    // Warning: (ae-forgotten-export) The symbol "ServerParseError" needs to be exported by the entry point index.d.ts
    // Warning: (ae-forgotten-export) The symbol "ServerError" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    networkError: Error | ServerParseError | ServerError | null;
    // (undocumented)
    protocolErrors: ReadonlyArray<GraphQLFormattedError>;
}

// @public (undocumented)
export interface ApolloErrorOptions {
    // (undocumented)
    clientErrors?: ReadonlyArray<Error>;
    // (undocumented)
    errorMessage?: string;
    // (undocumented)
    extraInfo?: any;
    // (undocumented)
    graphQLErrors?: ReadonlyArray<GraphQLFormattedError>;
    // (undocumented)
    networkError?: Error | ServerParseError | ServerError | null;
    // (undocumented)
    protocolErrors?: ReadonlyArray<GraphQLFormattedError>;
}

// @public (undocumented)
interface DefaultContext extends Record<string, any> {
}

// Warning: (ae-forgotten-export) The symbol "ExecutionPatchResultBase" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
interface ExecutionPatchIncrementalResult<TData = Record<string, any>, TExtensions = Record<string, any>> extends ExecutionPatchResultBase {
    // (undocumented)
    data?: never;
    // (undocumented)
    errors?: never;
    // (undocumented)
    extensions?: never;
    // Warning: (ae-forgotten-export) The symbol "IncrementalPayload" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    incremental?: IncrementalPayload<TData, TExtensions>[];
}

// @public (undocumented)
interface ExecutionPatchInitialResult<TData = Record<string, any>, TExtensions = Record<string, any>> extends ExecutionPatchResultBase {
    // (undocumented)
    data: TData | null | undefined;
    // (undocumented)
    errors?: ReadonlyArray<GraphQLFormattedError>;
    // (undocumented)
    extensions?: TExtensions;
    // (undocumented)
    incremental?: never;
}

// Warning: (ae-forgotten-export) The symbol "ExecutionPatchInitialResult" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "ExecutionPatchIncrementalResult" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
type ExecutionPatchResult<TData = Record<string, any>, TExtensions = Record<string, any>> = ExecutionPatchInitialResult<TData, TExtensions> | ExecutionPatchIncrementalResult<TData, TExtensions>;

// @public (undocumented)
interface ExecutionPatchResultBase {
    // (undocumented)
    hasNext?: boolean;
}

// Warning: (ae-forgotten-export) The symbol "SingleExecutionResult" needs to be exported by the entry point index.d.ts
// Warning: (ae-forgotten-export) The symbol "ExecutionPatchResult" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
type FetchResult<TData = Record<string, any>, TContext = Record<string, any>, TExtensions = Record<string, any>> = SingleExecutionResult<TData, TContext, TExtensions> | ExecutionPatchResult<TData, TExtensions>;

// Warning: (ae-forgotten-export) The symbol "FetchResult" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
type FetchResultWithSymbolExtensions<T> = FetchResult<T> & {
    extensions: Record<string | symbol, any>;
};

// @public @deprecated (undocumented)
export type GraphQLErrors = ReadonlyArray<GraphQLError>;

// Warning: (ae-forgotten-export) The symbol "FetchResultWithSymbolExtensions" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
export function graphQLResultHasProtocolErrors<T>(result: FetchResult<T>): result is FetchResultWithSymbolExtensions<T>;

// @public (undocumented)
interface IncrementalPayload<TData, TExtensions> {
    // (undocumented)
    data: TData | null;
    // (undocumented)
    errors?: ReadonlyArray<GraphQLFormattedError>;
    // (undocumented)
    extensions?: TExtensions;
    // (undocumented)
    label?: string;
    // Warning: (ae-forgotten-export) The symbol "Path" needs to be exported by the entry point index.d.ts
    //
    // (undocumented)
    path: Path;
}

// @public (undocumented)
export function isApolloError(err: Error): err is ApolloError;

// @public (undocumented)
export type NetworkError = Error | ServerParseError | ServerError | null;

// @public (undocumented)
type Path = ReadonlyArray<string | number>;

// @public (undocumented)
export const PROTOCOL_ERRORS_SYMBOL: unique symbol;

// @public (undocumented)
type ServerError = Error & {
    response: Response;
    result: Record<string, any> | string;
    statusCode: number;
};

// @public (undocumented)
type ServerParseError = Error & {
    response: Response;
    statusCode: number;
    bodyText: string;
};

// Warning: (ae-forgotten-export) The symbol "DefaultContext" needs to be exported by the entry point index.d.ts
//
// @public (undocumented)
interface SingleExecutionResult<TData = Record<string, any>, TContext = DefaultContext, TExtensions = Record<string, any>> {
    // (undocumented)
    context?: TContext;
    // (undocumented)
    data?: TData | null;
    // (undocumented)
    errors?: ReadonlyArray<GraphQLFormattedError>;
    // (undocumented)
    extensions?: TExtensions;
}

// (No @packageDocumentation comment for this package)

```
